---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "FitViz"
summary: "ANT+ Health and Fitness Monitoring Client"
authors: []
tags: ["Clinical Research"]
categories: ["Clinical Research"]
date: 2020-06-05T23:32:49-07:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption:
  focal_point: "Bottom"
  preview_only: false


  # Projects (optional).
  #   Associate this post with one or more of your projects.
  #   Simply enter your project's folder or file name without extension.
  #   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
  #   Otherwise, set `projects = []`.
  projects: []
---

{{< tabs tabTotal="2" tabID="1" tabName1="Overview" tabName2="Skills" >}}
{{< tab tabNum="1" >}}
#### Overview
FitViz is a monitoring client designed for fitness enthusiasts and gamers. It supports real-time visualization and tracking of health and fitness data sent from ANT+ devices. FitViz also provides networking capabilities allowing game developers to easily integrate ANT+ devices, such as bike trainers and heart rate monitors, into their own game.

The idea behind this project was to provide a standalone PC application that allowed me to interface with a Wahoo Kickr Snap bike trainer. In particular, I was interested in obtaining real-time measurements of speed and power from the Wahoo Kickr to be used as an input controller for a VR game.

#### About ANT+
ANT+ is a wireless sensor network technology that allows you to moniter data broadcast from ANT+ capable devices. Fitness equipment, bike trainers, heart rate monitors, and blood pressure monitors are just a few of the many devices supported within the ANT+ ecosystem. Data broadcast from ANT+ devices is standardized based on the type of data being sent. ANT+ refers to a data type as a device profile. An ANT+ device can broadcast data associated with multiple device profiles. For example, the Wahoo Kickr Snap broadcasts bicycle power and fitness equipment data.

### Video
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/Eyo31jKeFIw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

FitViz can be downloaded at: https://github.com/arsakhar/FitViz

{{< /tab >}}


{{< tab tabNum="2" >}}
#### Technical Skills

<ol>
  <li>ANT+ Communication</li>
    <ul style="list-style-type:square;">
      <li>Communicating with and reading sensor information from ANT+ devices</li>
    </ul>
  <li>Exporting Data</li>
    <ul style="list-style-type:square;">
      <li>Writing data to UDP port</li>
      <li>Saving data to CSV</li>
    </ul>
  <li>Visualization</li>
    <ul style="list-style-type:square;">
      <li>Developing GUI</li>
      <li>Displaying sensor values in real-time</li>
    </ul>
</ol>

#### Packages
<ol>
  <li>PyQt5</li>
  <li>LibAnt</li>
</ol>

{{< /tab >}}
