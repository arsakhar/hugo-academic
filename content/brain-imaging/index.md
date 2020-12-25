---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Brain Imaging"
type: "brain-imaging"
---

{{< tabs tabTotal="2" tabID="1" tabName1="Software" tabID="2" tabName2="Pipelines">}}


{{< tab tabNum="1" >}}
<br>
<b><u>NeuroFlow</u></b><br>
A brain imaging tool for analyzing cerebral flow dynamics. (<b><a href="/project/neuroflow/">Read</a></b>)

<a href="/project/neuroflow/"><img src="/project/neuroflow/featured.png" /></img></a>

{{< /tab >}}

{{< tab tabNum="2" >}}
<br>
The following are brain imaging pipelines I have used extensively as part of my research on aging and AD dementia. As a result, I have a strong background in visualizing, processing, and analyzing a number of different MRI modalities. This includes assessing brain morphometry on T1 and T2 images, as well as flow on PC-MRI images.

<br><br>
<b><u>Hippocampal Subfields</u></b><br>
<a href="https://www.nitrc.org/projects/ashs">ASHS</a> (external) is a tool for segmenting and labeling the hippocampal subfields and medial temporal lobe (MTL). The software uses T1 and T2 weighted MRI’s to segment the MTL and hippocampal subfields.<br><br>

<b>Purpose: </b> The entorhinal cortex, CA1, and CA4/dentate gyrus subfields of the hippocampus have been linked to aging and AD pathology and have also been shown to be important for spatial memory (Yushkevich PA., et al., 2014).

<img src="/brain-imaging/images/hippocampal_subfields.png" /></img>

<br>
<b><u>General Brain Morphometry</u></b><br>
<a href="https://surfer.nmr.mgh.harvard.edu/">Freesurfer</a> (external) is an open source software suite for processing and analyzing human brain MRI images. The software uses T1 MPRAGE images to segment the brain.<br><br>

<b>Purpose: </b> Studies have shown that whole brain volumes decrease approximately .45% per year in older adults (Fotenos Anthony F., et al., 2005).

<img src="/brain-imaging/images/freesurfer_segmentation.png" /></img>

<br>
<b><u>Cerebral Flow Dynamics</u></b><br>
<a href="https://github.com/arsakhar/NeuroFlow">NeuroFlow</a> (written by me) is a brain imaging tool for analyzing cerebral flow dynamics. Another, older option, is BioFlow (Balédent O, et al., 2001).<br><br>

<b>Purpose: </b> The cerebral aqueduct (CA) and C2-C3 region have been shown to be sensitive to the pathological changes that occur in aging and Alzheimer’s disease (El Sankari S., et al., 2011).

<img src="/brain-imaging/images/flow.png" /></img>

<br>
<b><u>Perivascular Spaces</u></b><br>
The PVS Pipeline is an in-house pipeline tool written by Dr. Farshid Sepehrband.
<br><br>

<b>Purpose: </b> Perivascular space size is associated with Alzheimer's disease (Banerjee G., et al., 2017)

<img src="/brain-imaging/images/pvs.png" /></img>

{{< /tab >}}

{{< /tabs >}}
