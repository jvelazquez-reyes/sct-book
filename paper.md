---
title: 'Image processing with Spinal Cord Toolbox (SCT)'
tags:
  - Spinal Cord Toolbox
  - Jupyter Book
  - Interactive tutorial
authors:
  - name: Mathieu Boudreau
    orcid: 0000-0002-7726-4456
    affiliation: "1, 2"
  - name: Julien Cohen-Adad
    orcid: 0000-0003-3662-9532
    affiliation: "1, 2"
affiliations:
 - name: NeuroPoly Lab, Institute of Biomedical Engineering, Polytechnique Montreal, Montreal, Canada
   index: 1
 - name: Montreal Heart Institute, University of Montréal, Montréal, Canada
   index: 2
date: 11 October 2021
bibliography: paper.bib
---

# Summary

In this interactive notebook we will go through a series of processing steps specific to spinal cord MRI analysis. We will be using the [Spinal Cord Toolbox (SCT)](https://github.com/neuropoly/spinalcordtoolbox), lead by Prof. Julien Cohen-Adad and the [NeuroPoly](https://www.neuro.polymtl.ca) lab at Polytechnique de Montréal. The main goal is to demonstrate an end-to-end template-based analysis pipeline, where we start of with the raw NIFTI data and end up with quantitative metrics. Here, the metric will be magnetization transfer saturation (MTsat) extracted in specific white matter tracts. 

# Acknowledgements

NeuroLibre is sponsored by Canadian Open Neuroscience Platform (CONP), Brain Canada, Quebec Bioimaging Network, Cancer Computing and Healthy Brains & Healthy Life. 
