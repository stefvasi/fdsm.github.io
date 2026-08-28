---
layout: post
title: "Navigating Sleep: Neural Audio Synthesis as Compositional Medium for EEG Data Sonification"
author: "SS"
categories: research
tags: [research, sonification, EEG, neural-audio, RAVE, ICAD]
image: Navigating_Sleep_post/poster.jpg
---

*Navigating Sleep* is a practice-based study of neural audio synthesis as a compositional medium for the sonification of physiological time-series data. It takes one night of sleep EEG and turns it into sound by driving the latent spaces of pre-trained <a href="https://github.com/acids-ircam/RAVE">RAVE</a> neural-synthesis models. The work was presented at <a href="https://interactive-sonification.org/icad2026/">ICAD 2026</a>, the International Conference on Auditory Display, and grew out of my MSc thesis, developed between the <a href="https://iil.is">Intelligent Instruments Lab</a> (University of Iceland) and the Laboratory of Music Acoustics and Technology (LabMAT), National and Kapodistrian University of Athens.

<br>

The source data come from the Bitbrain Open Access Sleep dataset — a full night of polysomnography from a single subject, recorded across six scalp electrodes. For each electrode the pipeline estimates spectral power in five EEG bands (delta, theta, alpha, sigma, beta) with Welch's method, spectrally flattens it, and reduces it to five principal components that track how each spectrum moves through the night.

The <a href="https://stefvasi.github.io/Navigating_Sleep/navigating_sleep_icad2026.pdf">extended abstract (PDF)</a> is available online.

<br>

## Listen

<div class="audio-block" markdown="0">
  <p><strong>The full composition</strong> — the night in ~14:20, at 30:1. Sleep stages gate which electrode–model pair sounds.</p>
  <audio controls preload="none" style="width:100%">
    <source src="https://stefvasi.github.io/Navigating_Sleep/audio/Navigating-Sleep-composition.mp3" type="audio/mpeg">
  </audio>

  <p><strong>Voices soundscape</strong> — the full night through the voice model, unedited.</p>
  <audio controls preload="none" style="width:100%">
    <source src="https://stefvasi.github.io/Navigating_Sleep/audio/Navigating-Sleep-voices.mp3" type="audio/mpeg">
  </audio>

  <p><strong>Organ soundscape</strong> — the full night through the organ model, unedited.</p>
  <audio controls preload="none" style="width:100%">
    <source src="https://stefvasi.github.io/Navigating_Sleep/audio/Navigating-Sleep-organ.mp3" type="audio/mpeg">
  </audio>
</div>

The <a href="https://stefvasi.github.io/Navigating_Sleep/">full listen page</a> also collects short excerpts around specific sleep-stage transitions — sleep onset, first deep sleep, first REM, a sustained REM block, a deep-sleep arousal, the ending, and a full NREM–REM cycle — each in all three model variants.

<br>

## Credits

By Stefanos Vasilakis, in collaboration with Areti Andreopoulou and Thanos Polymeneas Liontiris. The RAVE models were trained at the Intelligent Instruments Lab, University of Iceland.
