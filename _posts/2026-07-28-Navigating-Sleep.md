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

## From EEG to a learned sound

The source data come from the Bitbrain Open Access Sleep dataset — a full night of polysomnography from a single subject, recorded across six scalp electrodes. For each electrode the pipeline estimates spectral power in five EEG bands (delta, theta, alpha, sigma, beta) with Welch's method, spectrally flattens it, and reduces it to five principal components that track how each spectrum moves through the night.

Those components are not mapped to synthesis parameters in the usual sense. Instead they are written directly into the *latent space* of a RAVE model, bypassing the encoder. Where the everyday use of such a model is timbre transfer — audio in, transformed audio out — here the sleep data itself becomes a position inside the model's learned sound manifold. This is closer to *latent-space navigation* than to conventional parameter-mapping sonification: the data steers a trajectory through a space of sounds the network has learned, and the output is whatever the decoder makes of that position. Three pre-trained models were used — a *voice* model, an *organ* model, and a *modular*-synthesizer model. The whole night is time-compressed 30:1, folding roughly seven hours of sleep into about fourteen minutes.

<br>

## Signal and symbol

The composition is organised around the signal/symbol framework of Crozzoli's *Dark Sonification* [1]. The continuous flow of bandpower data is the *signal*; the sleep stages — Wake, N1, N2, N3, REM — act as *symbolic* markers layered on top of it. The stages gate which electrode–model pair is audible at any given moment, so the architecture of the night becomes the structural backbone of the piece. The project resulted in three outputs: two full-night soundscapes that document the raw data–model interaction unedited, and a final composition in which the sleep stages decide what is audible — the point at which data-driven material meets compositional agency.

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

## Poster

<div class="gallery gallery-single" markdown="0">
  <a href="/assets/img/Navigating_Sleep_post/poster.jpg" class="glightbox">
    <img loading="lazy" src="/assets/img/Navigating_Sleep_post/poster.jpg" alt="Navigating Sleep — ICAD 2026 A1 poster">
  </a>
</div>

The <a href="https://stefvasi.github.io/Navigating_Sleep/navigating_sleep_icad2026.pdf">extended abstract (PDF)</a> and the <a href="https://github.com/stefvasi/Navigating_Sleep">project repository</a> are both online.

<br>

## Credits

By Stefanos Vasilakis, in collaboration with Areti Andreopoulou and Thanos Polymeneas Liontiris. The RAVE models were trained at the Intelligent Instruments Lab, University of Iceland.

<br>

## References

[1] Crozzoli, M.A. (2025) "Dark Sonification: An Entangled Post-Interaction Multimodal Data Display System," in *Doctoral Consortium, Sixth Decennial Aarhus Conference*. Available at: <a href="https://hal.science/hal-05191041">https://hal.science/hal-05191041</a>

[2] Caillon, A. and Esling, P. (2021) "RAVE: A Variational Autoencoder for Fast and High-Quality Neural Audio Synthesis," *arXiv:2111.05011*. Available at: <a href="https://arxiv.org/abs/2111.05011">https://arxiv.org/abs/2111.05011</a>

[3] López-Larraz, E. et al. (2025) "Bitbrain Open Access Sleep Dataset," *OpenNeuro*. Available at: <a href="https://doi.org/10.18112/OPENNEURO.DS005555.V1.1.0">https://doi.org/10.18112/OPENNEURO.DS005555.V1.1.0</a>
