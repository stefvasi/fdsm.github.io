---
layout: post
title: "Octopus: A Modular Haptic Feedback Interface"
author: "SS"
categories: research
tags: [research, hardware, haptics, open-source]
image: Octopus_main_post/Octopus_post.png
---

The project explores the design and development of an open-ended, modular hardware/software interface named "Octopus" to expand research in multi-modal data exploration. The system is designed for integration with the "Dark Sonification" framework developed by PhD researcher <a href="https://crozzoli.com/">Miguel Angel Crozzoli</a>, an interactive data display system for exploratory data analysis through affect, and focuses on applying data physicalization techniques through haptic feedback. "Octopus" is an open-source, customizable device that provides an embodied interface for data navigation and interaction. By bridging the gap between flexible software and reconfigurable hardware, the project contributes to the emerging field of Data-Human Interaction and addresses the societal need for accessible and inclusive scientific tools. The interface's design emphasizes versatility, enabling researchers to rapidly prototype new ideas and integrate novel sensory modalities for enhanced data understanding. The project is inspired by the sensory system of the octopus whose tentacles are capable of different sensory modalities including touch, taste, smell and chemical analysis.

<br>

## The "Octopus" interface

"Octopus" is an affordable and simple-to-build, autonomous portable technology providing input and output for interfacing physically with data displays in Python programming language. The system consists of two modules: the translator and the communication node. Seven "tentacles" can be attached to the communication node, one of which acts as an input and 6 as output. As input, an Inertial Measurement Unit (IMU) provides 3-D orientation and acceleration measurements, which enables spatial navigation by tilting the wrist, although any digital sensor capable of I2C communication can be used. The output provides for haptic feedback with 6 channels of linear resonant acceleration (LRA) discs that can be configured and driven independently. The "tentacles" connect to the communication unit with TRRS connectors. The translator unit connects to a computer via USB and transfers data between the data display and communication node with the OSC protocol over Serial. The data transmission between the communication node and the translator is wireless via the ESPNow protocol. The communication node runs on battery and its autonomy is estimated, depending on the configuration, from 5 to 11 hours. The Python library for data transmission between "Octopus" and data display, code necessary for programming both units, and 3D printing files are open access and available on the <a href="https://github.com/stefvasi/Octopus#">project's page on Github</a>.

<br>

<div class="gallery" markdown="0">
  <img src="/assets/img/Octopus_main_post/sleeve_on.png" alt="Octopus wearable sleeve">
  <img src="/assets/img/Octopus_main_post/com_node.png" alt="Octopus communication node">
</div>

<div class="gallery" markdown="0">
  <img src="/assets/img/Octopus_main_post/sleeve_1.jpg" alt="Octopus sleeve detail">
  <img src="/assets/img/Octopus_main_post/trans_unit.png" alt="Octopus translator unit">
</div>

<div class="gallery gallery-single" markdown="0">
  <img src="/assets/img/Octopus_main_post/inputs.png" alt="Octopus input modules">
</div>

<br>

"Octopus" is designed on purpose to be versatile and customizable. It serves as an interface that helps connect data with physical exploration, by mapping the data into a physical artifact that can be sculpted into different geometries, enabling an embodied experience. As such, "Octopus" allows for easy deployment of artifacts for interactive data exploration through tactile engagement. Additionally, "Octopus" is designed to support multiple wearable devices interacting with the same dataset, providing for collaborative data exploration. The configuration of the haptic feedback has three variables: vibrator index, intensity, and duration. The optimal frequency for the vibration of the LRA is the resonant frequency of the system and it's defined by the hardware's physical characteristics.

<br>

The development of the project took place in the summer of 2025 at the <a href="https://iil.is">Intelligent Instruments Lab</a>, University of Iceland, and has been funded by <a href="https://en.rannis.is/funding/research/icelandic-student-innovation-fund/">Rannis</a>' Student Innovation Fund and was realised in collaboration with the PhD researcher <a href="https://crozzoli.com/">Miguel Angel Crozzoli</a>.

<br>

## References

[1] Crozzoli, M.A. (2025) "Dark Sonification: an Entangled Post-Interaction Multimodal Data Display System," in Doctoral Consortium at the sixth decennial Aarhus conference: Computing X Crisis. Aarhus, Denmark. Available at: <a href="https://hal.science/hal-05191041">https://hal.science/hal-05191041</a>

[2] Crozzoli, M.A. and Magnusson, T. (2025) "Data Perceptualization through Affect in Dark Sonification." Available at: <a href="https://doi.org/10.34626/2025_XCOAX_013">https://doi.org/10.34626/2025_XCOAX_013</a>

<div class="logo-row" markdown="0">
  <img src="/assets/img/iil_wordmark.jpg" alt="Intelligent Instruments Lab logo">
  <img src="/assets/img/rannis_logo_2.png" alt="Rannis logo">
</div>
