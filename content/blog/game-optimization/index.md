---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Unity3D - Performance Optimization"
subtitle: ""
summary: "Tips for optimizing performance on virtual reality games built with Unity3D"
authors: []
tags: ["Virtual Reality"]
categories: ["Virtual Reality"]
date: 2019-08-08T22:42:40-07:00
lastmod: 2019-08-08T22:42:40-07:00
featured: false
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: ["sals-sanctuary", "wildlife-enclosure"]
---

{{< tabs tabTotal="6" tabID="1" tabName1="Background" tabName2="Garbage Collection" tabName3="Polygon Count" tabName4="Draw Calls" tabName5="Camera Culling" tabName5="Static Batching" tabName6="References" >}}

{{< tab tabNum="1" >}}
### Background
The majority of VR headsets on the market use a 90 Hz refresh rate, such that the display on the headset is refreshed every 11 ms. Dropped frames will occur if the computer is unable to render an image within that time frame. API’s employ several techniques to account for dropped frames. These include timewarp, asynchronous timewarp, interleaved reprojection, motion smoothing, and positional timewarp.<sup>4</sup> While these techniques account for dropped frames to a certain extent, a poorly optimized game will still result in jittery views which can be quite nauseogenic. Therefore, performance optimization is a key component of game development. In this article, I will provide a brief overview of the most common techniques used to optimize performance. I will also provide links that provide a more in-depth discussion of each technique. Please note that this is not an exhaustive list of performance tips, rather a list of low hanging fruit a develop can use to get substantial improvements in performance.
{{< /tab >}}


{{< tab tabNum="2" >}}
### Garbage Collection
Garbage collection (GC) is a form of automated memory management.<sup>1</sup> There are two types of memory allocation: heap and stack. Furthermore, there are two data types: primitive and non-primitive.<sup>3</sup> Primitive data types include the following: bool, bytes, short, int, long, float, double, decimal, and char. All primitive data type values are stored in stack memory. Non-primitive data types are objects and include the following: class, struct, enum, array, and string. Non-primitive data types are known as reference types, as the stack memory only contains a reference to the value. The reference in the stack points to an object located in heap memory that contains the value . GC only track objects (non-primitive data types) that occupy space in heap memory.<sup>2</sup> The job of GC is to free memory when the object is no longer being referenced in the stack memory.

Unity uses the Boehm–Demers–Weiser GC5, which is a type of stop-the-world GC. This means that when GC is required, code execution will stop until the GC process is complete. Depending on the frequency of GC, this can result in dropped frames and significantly affect the smoothness of gameplay. The figure below illustrates code that minimizes garbage collection (GoodExample) and unnecessarily increases garbage collection (BadExample).


In the bad example, we are instantiating a new WaitForSeconds routine every second. This results in a heap memory allocation every time an instance of WaitForSeconds is created. Each heap memory allocation is going to trigger a garbage collection. To minimize garbage collection, a single instance of WaitForSeconds can be used used if the wait period is the same each time.

Further Reading:<br>
https://jacksondunstan.com/articles/2981
http://blog.tochasstudios.com/2015/11/cache-coroutines.html
https://forum.unity.com/threads/c-coroutine-waitforseconds-garbage-collection-tip.224878/
{{< /tab >}}


{{< tab tabNum="3" >}}
### Polygon Count
The primary responsibility of the GPU is to render an image to the screen. The complexity of an image can significantly impact rendering performance. In VR, the images that are rendered are 3D meshes. Briefly, all meshes are composed of smaller units known as polygons, which can be further decomposed into triangles. Triangles consist of vertices whose positions can be stored as an array of values (x,y,z). During rendering, the GPU first uses a vertex shader to compute where the triangle should be placed on the screen and then uses a fragment shader to fill in the pixels (rasterize) within the vertices of the triangle.<sup>6</sup> With modern GPU’s, polygon counts aren’t typically a bottleneck for performance. However, it’s still good practice for developers to simplify meshes in situations where detailed renderings aren’t needed. Blender is a free 3D modeling program that has the ability to simplify a mesh using the decimate function.

Further Reading:<br>
http://software.intel.com/en-us/articles/model-for-real-time-beyond-counting-polygons/
{{< /tab >}}


{{< tab tabNum="4" >}}
### Draw Calls
A draw call is an instruction sent from the CPU to the GPU to render an image to the screen. An excessive number of draw calls can bottleneck the CPU if it is unable to push all draw call instructions to the GPU within that frame. In Unity, a draw call is required any time the GPU has to render a material. Multiple materials can be assigned to a single mesh, while a single diffuse texture is typically assigned to each material. A mesh consisting of 4 materials would require 4 separate draw calls from the CPU. The number of draw calls can be minimized by combining multiple meshes into a single mesh and applying a single material to that mesh. The use of a single material is possible through texture atlases, which map out how a texture is laid onto a material. MeshBaker on the Unity Asset Store is a popular asset that allows user’s to combine meshes and create texture atlases.<sup>7</sup>

Further Reading:<br>
https://medium.com/@toncijukic/draw-calls-in-a-nutshell-597330a85381
{{< /tab >}}


{{< tab tabNum="5" >}}
### Camera Culling
By default, the camera in the game will render everything within its FOV. However, this is not always necessary as the user’s viewing depth is typically limited by vegetation, buildings, and other objects within the scene. Consider setting a culling distance such that any objects past that distance are not rendered. Game objects can even be assigned to different layers and a separate culling distance can be used for each layer. For example, flowers may require a shorter culling distance while larger landmarks may require a larger culling distance.

Further Reading:<br>
https://docs.unity3d.com/ScriptReference/Camera-layerCullDistances.html
{{< /tab >}}


{{< tab tabNum="6" >}}
### Static Batching
For any object that isn’t moving in the environment, enable static batching. This combines all meshes that have the same material into 1 and renders it in 1 draw call. The negative is increased memory overhead. However, the advantage of this over consolidating into 1 mesh is that you can still cull each object individually.
{{< /tab >}}


{{< tab tabNum="7" >}}
### References
1. “Garbage collection (computer science) – Wikipedia.” [Online]. Available: https://en.wikipedia.org/wiki/Garbage_collection_(computer_science). [Accessed: 19-Jun-2019].
2. “Feature Preview: Incremental Garbage Collection – Unity Blog.” [Online]. Available: https://blogs.unity3d.com/2018/11/26/feature-preview-incremental-garbage-collection/. [Accessed: 19-Jun-2019].
3. “C# Variables: Primitive and Non-primitive Types.” [Online]. Available: http://www.jeremyshanks.com/c-variables-primitive-nonprimitive-types/. [Accessed: 19-Jun-2019].
4. D. Heaney, D. Jagneaux, J. Feltham, and J. Feltham, “VR Timewarp, Spacewarp, Reprojection, And Motion Smoothing Explained,” UploadVR, 18-Jan-2019. [Online]. Available: https://uploadvr.com/reprojection-explained/. [Accessed: 15-Jul-2019]
5. A garbage collector for C and C++. (2019). Retrieved from https://www.hboehm.info/gc/
6. Eskil_steenberg. “Model for Real Time-Beyond Counting Polygons.” Intel® Software, Intel, 15 Dec. 2018, software.intel.com/en-us/articles/model-for-real-time-beyond-counting-polygons.
7. Digital Opus, digitalopus.ca/site/mesh-baker/.
{{< /tab >}}
{{< /tabs >}}
