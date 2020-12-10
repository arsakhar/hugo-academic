---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "NeuroFlow"
summary: "A brain imaging tool for analyzing cerebral flow dynamics"
authors: []
tags: ["Brain Imaging"]
categories: ["Brain Imaging"]
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
NeuroFlow is an imaging tool that allows neuroscientists and clinicians to analyze cerebral flow dynamics in the brain. The continuous circulation of cerebrospinal fluid (CSF) and cerebral blood flow (CBF) is key to the health of our central nervous system. When CSF and CBF dynamics in the brain become dysregulated, pathophysiological states can occur. As such, cerebral flow dynamics may be an important biomarker for identifying meaningful alterations in neurological diseases.

Phase-contrast MRI (PC-MRI) is a validated, non-invasive MRI imaging technique, allowing rapid measurements of CSF and CBF flow in the brain. NeuroFlow provides a user-friendly interface for neuroscientists and clinicians to analyze PC-MRI images and extract measurements associated with cerebral flow dynamics. Moreover, NeuroFlow provides numerous tools to help user's quickly, accurately, and painlessly analyze flow data.

NeuroFlow can be downloaded at: https://github.com/arsakhar/NeuroFlow

{{< /tab >}}


{{< tab tabNum="2" >}}
#### Technical Skills

<ol>
  <li>Reading and Loading DICOMDIR</li>
    <ul style="list-style-type:square;">
      <li>Storing Patient, Study, Series, Sequence, and Image information entities of the DICOM data model in accordance with the NEMA DICOM standard.</li>
    </ul>
  <li>Image Segmentation</li>
    <ul style="list-style-type:square;">
      <li>Providing tools for users to segment and label ROI’s on an image</li>
    </ul>
  <li>Visualization</li>
    <ul style="list-style-type:square;">
      <li>Developing GUI</li>
      <li>Displaying Graphs, Images, Tables, and DICOM Metadata</li>
    </ul>
  <li>Image Classification</li>
    <ul style="list-style-type:square;">
      <li>Training a CNN to classify MRI scans according to anatomical level in the brain</li>
    </ul>
</ol>

#### Packages
<ol>
  <li>PyQt5</li>
  <li>NumPy</li>
  <li>Pandas</li>
  <li>PyQtGraph</li>
  <li>PIL</li>
  <li>CV2</li>
  <li>Torch</li>
  <li>TorchVision</li>
  <li>Matplotlib</li>
  <li>Pydicom</li>
</ol>

{{< /tab >}}
