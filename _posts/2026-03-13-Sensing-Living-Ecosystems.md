---
layout: post
title: "Sensing Living Ecosystems"
author: "SS"
categories: research
tags: [research, hardware, plants, sensing, open-source]
image: Vegetal_Media_post/vegetal_kit_detail.jpg
---

*Development of technological mediation between humans and plants.*

<br>

**Sensing Living Ecosystems** develops the *Greenhouse Field Kit* — an open hardware/software system for sensing the conditions plants live in and turning them into data we can read and work with. It treats a greenhouse or garden as a continuously changing field of light, gas, heat and moisture, and builds low-cost tools to make that field measurable.

<br>

## The Greenhouse Field Kit

The *Vegetal Media Greenhouse Field Kit* is an affordable, open hardware sensor node built around an Adafruit QT Py ESP32-S2, with five environmental sensors on a single I²C chain covering air, light, surface and soil:

- **Air** — CO₂, temperature and humidity (Sensirion SCD30)
- **Light** — full-spectrum, infrared and lux (TSL2591)
- **Spectral** — ten channels from 415–680 nm plus Clear and near-infrared (AS7341)
- **Surface temperature** — non-contact infrared thermometer (Melexis MLX90632)
- **Soil** — capacitive soil moisture and soil temperature (Adafruit STEMMA Soil Sensor)

The node is headless: it samples every 500 ms to a local microSD archive and publishes over WiFi every two seconds via MQTT. Readings can be streamed live into Python, TouchDesigner or Max, or pushed through a cloud pipeline (HiveMQ → InfluxDB → Grafana). The full archive stays on the SD card, so the kit keeps recording with or without a network. A 3D-printed mount holds the sensors in a fixed geometry so readings stay comparable between kits. Firmware, Python tools, the printable mount and the build guide are open access.

<br>

<div class="gallery" markdown="0">
  <img src="/assets/img/Vegetal_Media_post/vegetal_hero.jpg" alt="The field kit set up in a tropical greenhouse">
  <img src="/assets/img/Vegetal_Media_post/vegetal_kit_greenhouse.jpg" alt="The field kit among greenhouse plants">
</div>

<br>

## In the greenhouse

The kit was first set up inside a tropical greenhouse, logging CO₂, the spectrum of light through the glass, and the temperature of leaves and soil.

<br>

<div class="gallery" markdown="0">
  <img src="/assets/img/Vegetal_Media_post/vegetal_greenhouse_wide.jpg" alt="The field kit logging data inside a lush greenhouse">
  <img src="/assets/img/Vegetal_Media_post/vegetal_banana_flower.jpg" alt="A flowering banana plant in the greenhouse">
</div>

<br>

## Out in the field

Sealed into a weatherproof enclosure, the same kit can be deployed outdoors — here at the base of a banana tree — to monitor air, light and soil over longer stretches. The hardware is low-cost and replicable, so several nodes can be distributed across an ecosystem.

<br>

<div class="gallery" markdown="0">
  <img src="/assets/img/Vegetal_Media_post/vegetal_deploy_banana.jpg" alt="The weatherproofed kit deployed at the base of a banana plant">
  <img src="/assets/img/Vegetal_Media_post/vegetal_deploy_field.jpg" alt="The Vegetal Media kit and enclosure deployed in the field">
</div>

<br>

*Vegetal Media* is part of the wider *organium* family of open components developed at the Intelligent Instruments Lab. By making the sensing of plant environments cheap, open and reproducible, it gives artists and researchers a shared basis for work on data perceptualization and the relationship between humans and plants.

<br>

The field kit was built to support the doctoral research of <a href="https://iil.is/people">Thomas Pausz</a>, whose PhD project at the lab is itself titled *Vegetal Media*. The project was developed at the <a href="https://iil.is">Intelligent Instruments Lab</a>, University of Iceland, and is funded by the University of Iceland Research Fund (Rannsóknasjóður Háskóla Íslands). Component reference and the wider organium family: <a href="http://iil.is/organium-elements/">iil.is/organium-elements</a>.

<br>

## References

[1] Intelligent Instruments Lab (2024) "Organium," <i>AudioMostly 2024</i>. Available at: <a href="https://iil.is/pdf/2024_audiomostly_organium.pdf">https://iil.is/pdf/2024_audiomostly_organium.pdf</a>

<div class="logo-row" markdown="0">
  <img src="/assets/img/iil_wordmark.jpg" alt="Intelligent Instruments Lab logo">
  <img src="/assets/img/Vegetal_Media_post/hi_logo_white.png" alt="University of Iceland (Háskóli Íslands) logo">
</div>
