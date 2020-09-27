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

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

<b>Overview</b><br>
FitViz is a monitoring client designed for fitness enthusiasts and gamers. It supports real-time visualization and tracking of health and fitness data sent from ANT+ devices. FitViz also provides networking capabilities allowing game developers to easily integrate ANT+ devices, such as bike trainers and heart rate monitors, into their own game.

The idea behind this project was to provide a standalone PC application that allowed me to interface with a Wahoo Kickr Snap bike trainer. In particular, I was interested in obtaining real-time measurements of speed and power from the Wahoo Kickr to be used as an input controller for a VR game.

<b>About ANT+</b><br>
ANT+ is a wireless sensor network technology that allows you to moniter data broadcast from ANT+ capable devices. Fitness equipment, bike trainers, heart rate monitors, and blood pressure monitors are just a few of the many devices supported within the ANT+ ecosystem. Data broadcast from ANT+ devices is standardized based on the type of data being sent. ANT+ refers to a data type as a device profile. An ANT+ device can broadcast data associated with multiple device profiles. For example, the Wahoo Kickr Snap broadcasts bicycle power and fitness equipment data.

FitViz can be downloaded at: https://github.com/arsakhar/FitViz
