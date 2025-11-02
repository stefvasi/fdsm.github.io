---
layout: post
title: "Octopus: a modular haptic feedback interface"
author: "SS"
categories: research
tags: [research]
image: /Octopus_main_post/Octopus_post.png
---


<br>
The project explores the design and development of an open-ended, modular hardware/software interface named "Octopus" to expand research in multi-modal data exploration. The system is designed for integration with the "Dark Sonification" framework [[1]](#Crozzoli_2025) developed by PhD researcher <a href="https://crozzoli.com/">Miguel Angel Crozzoli</a>, an interactive data display system for exploratory data analysis through affect [[2]](#Crozzoli_Magnusson_2025), and focuses on applying data physicalization techniques through haptic feedback. "Octopus" is an open-source, customizable device that provides an embodied interface for data navigation and interaction. By bridging the gap between flexible software and reconfigurable hardware, the project contributes to the emerging field of Data-Human Interaction and addresses the societal need for accessible and inclusive scientific tools. The interface’s design emphasizes versatility, enabling researchers to rapidly prototype new ideas and integrate novel sensory modalities for enhanced data understanding.
The project is inspired by the sensory system of the octopus whose tentacles are capable of different sensory modalities including touch, taste, smell and chemical analysis.

## The “Octopus” interface 

“Octopus” is an affordable and simple-to-build, autonomous portable technology providing input and output for interfacing physically with data displays in Python programming language. The system consists of two modules: the translator (Fig. 2) and the communication node (Fig. 4). Seven “tentacles” can be attached to the communication node, one of which acts as an input and 6 as output (Fig. 1). As input, an Inertial Measurement Unit (IMU) provides 3-D orientation and acceleration measurements, which enables spatial navigation by tilting the wrist, although any digital sensor capable of I2C communication can be used. The output provides for haptic feedback with 6 channels of linear resonant acceleration (LRA) discs that can be configured and driven independently. The “tentacles” connect to the communication unit with TRRS connectors (Fig. 5). The translator unit connects to a computer via USB and transfers data between the data display and communication node with the OSC protocol over Serial. The data transmission between the communication node and the translator is wireless via the ESPNow protocol. The communication node runs on battery and its autonomy is estimated, depending on the configuration, from 5 to 11 hours. The Python library for data transmission between “Octopus” and data display, code necessary for programming both units, and 3D printing files are open access and available on the <a href="https://github.com/stefvasi/Octopus#">project’s page on Github</a>.

“Octopus” is designed on purpose to be versatile and customizable. It serves as an interface that helps connect data with physical exploration, by mapping the data into a physical artifact that can be sculpted into different geometries, enabling an embodied experience. As such, “Octopurs” allows for easy deployment of artifacts for interactive data exploration through tactile engagement. Additionally, “Octopus” is designed to support multiple wearable devices interacting with the same dataset, providing for collaborative data exploration. The configuration of the haptic feedback has three variables: vibrator index, intensity, and duration. The optimal frequency for the vibration of the LRA is the resonant frequency of the system and, it’s defined by the hardware's physical characteristics. 

The development of the project took place in the summer of 2025 at the <a href="https:\\iil.is">Intelligent Instruments Lab</a>, University of Iceland, and has been funded by <a href="https://en.rannis.is/funding/research/icelandic-student-innovation-fund/">Rannis' Student Innovation Fund</a> and was be realised in collaboration with the PhD researcher <a href="https://crozzoli.com/">Miguel Angel Crozzoli</a>. 

![Translator_Unit](/assets/img/Octopus_main_post/sleeve_on.png)
Fig. 1 - Sleeve		   	  

![Communication_Node](/assets/img/Octopus_main_post/com_node.png)
Fig 2 - Communication Node
![Communication_Node](/assets/img/Octopus_main_post/sleeve_1.jpg)
Fig 3 - Communication Node
![Translator](/assets/img/Octopus_main_post/trans_unit.png)
Fig 4 - Tranlator

![Translator](/assets/img/Octopus_main_post/inputs.png)
Fig 5 - Tranlator


### References

 <a name="Crozzoli_2025">[1]</a> Crozzoli, M.A. (2025) “Dark Sonification: an Entangled Post-Interaction Multimodal Data Display System,” in Doctoral Consortium at the sixth decennial Aarhus conference: Computing X Crisis. Aarhus, Denmark. Available at: https://hal.science/hal-05191041 (Accessed: September 22, 2025). 

<a name="Crozzoli_Magnusson_2025">[2]</a> Crozzoli, M.A. and Magnusson, T. (2025) “Data Perceptualization through Affect in Dark Sonification.” Available at: https://doi.org/10.34626/2025_XCOAX_013

<div style="display: flex;">
    <div style="flex: 1; padding-right: 10px;">
      <img src="/assets/img/iil_wordmark.jpg" alt="iil_logo" style="width: 100%; height: auto;">
    </div>
    <div style="flex: 1; padding-left: 10px; padding-top: 20px;">
      <img src="/assets/img/rannis_logo_2.png" alt="rannis_logo" style="width: 100%; height: auto;">
    </div>
</div>


