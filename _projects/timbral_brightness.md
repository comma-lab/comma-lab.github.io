---
layout: page
title: Brightness Perception of Musical Sounds
description: 2020–present
img: /assets/img/projects/strauss_spectrogram_kai.png
order: 10
redirect: false
display: true
---

<img src="/assets/img/projects/bright_sounds.png" alt="spectrograms of four instruments" align="right" width="480"/> Timbre is commonly described using vision terms. Auditory brightness is among the most studied “[metaphors we listen with](/projects/timbre_metaphors/)” and arguably among the most important musical cues actively shaped by performers, composers, and audio engineers. 

Psychoacoustically, sounds described as ”bright” vs “dull” or ”dark” typically exhibit a high vs low frequency emphasis in the spectrum (see side figure with spectrograms of four acoustic instrument notes, f0 = 311 Hz, mezzo-forte, loudness matched). However, relatively little is known about the perceptual and neurocognitive mechanisms that facilitate using a visual quality to talk about something that sounds. The following studies set out to explore related questions. <br clear="left"/>

<h4><br>Relation to timbre dissimilarity and source-cause categories</h4>

<!-- Timbre dissimilarity of orchestral sounds is well-known to be multidimensional, with attack time and spectral centroid representing its two most robust acoustical correlates. The centroid dimension is traditionally considered as reflecting timbral brightness. In this study, we posed three important, yet unexplored questions: 
* the first question concerned the dimensionality of brightness as an attribute of timbre. Specifically, we wondered about the dimensionality that timbral brightness would exhibit as an auditory attribute in and of itself if considered through the empirical angle of pairwise dissimilarity ratings of a set of sounds.
* The second related question concerned the robustness (or stability) of brightness judgments across different tasks. Specifically, we wondered about the extent to which direct brightness ratings of a set of sounds would recover their ordering along the SC dimension obtained from general timbre dissimilarity ratings of the same sounds.
* The third question concerned the relation of brightness to source-cause categories. Specifically, we wondered whether brightness dissimilarity ratings of instrumental sounds would be affected by categorical stimulus features related to instrument family membership and the type of resonator and excitation. -->

<img src="/assets/img/projects/jasa2020_mushra.png" alt="mushra direct brightness ratings" align="right" width="480"/> [Saitis and Siedenburg (2020)](https://comma.eecs.qmul.ac.uk/assets/pdf/2256_1_final_published.pdf) used a triangulation approach to examine the dimensionality of timbral brightness, its robustness across different psychoacoustical contexts, and its relation to perception/recognition of the sounds' source-cause. Listeners compared 14 acoustic instrument sounds in three distinct tasks that collected general dissimilarity, brightness dissimilarity, and direct multi-stimulus brightness ratings. For the latter, we adapted the MUSHRA procedure (ITU-R BS.1534-3), whereby listeners are allowed to switch between multiple stimuli presented in parallel as often as they want, effectively performing a direct rating of each stimulus plus a ranking and inherently also pairwise comparisons. 

<!-- <img src="/assets/img/projects/jasa2020_exp_design.png" alt="methodology" width="420"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="/assets/img/projects/jasa2020_mushra.png" alt="mushra direct brightness ratings" width="440"/> -->

**Nonmetric multidimensional scaling** of the dissimilarity ratings produced a 2D brightness space (BRdissim), which was compared with a general timbre space (GEdissim), see left figure below. BRdissim's first dimension reflected spectral envelope, mirroring GEdissim's second dimension. Spectral centroid (SC) and log attack time (LAT) served as confirmatory descriptors (black correlations = SC; red = LAT). SC correlated with the dimensions as expected; however, somewhat surprisingly, LAT also correlated well with BRdissim's second dimension. This finding could suggest a leakage of GEdissim into BRdissim, which, like source-cause categories (see below), may further relate to the susceptibility of pairwise dissimilarity ratings to conflate other processes.

**Partial least-squares regression** models were used to predict GEdissim and BRdissim ratings from either acoustic descriptors or source-cause categorical predictors (resonator type, excitation type, instrument family), or their combination, see right figure below. For GEdissim, we replicated [earlier findings](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2015.01977/full) showing that musicians incorporate source-cause knowledge when judging general timbre dissimilarity. For BRdissim, the acoustic model performed best (85%); categorical predictors were much weaker (40% variance explained) and adding them to the acoustic model yielded no meaningful improvement. This suggests brightness is driven by acoustical rather than source-causal similarity. Disentangling spectral and temporal contributions to brightness perception would require synthetic stimuli with carefully dissociated properties. 

<img src="/assets/img/projects/jasa2020_spaces.png" alt="multidimensional scaling" width="430"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="/assets/img/projects/jasa2020_plsr.png" alt="partial least squares regression" width="430"/><br><br>

<h4><br>Timbral brightness perception investigated through multimodal interference</h4>

<img style="border:2px solid #555" src="/assets/img/projects/app_exp_design.png" alt="methodology" align="right" width="300"/> Also triangulating three different interaction paradigms, [Saitis and Wallmark (2024)](https://comma.eecs.qmul.ac.uk/assets/pdf/s13414-024-02934-2.pdf) investigated using speeded classification whether intramodal, crossmodal, and amodal interference occurs when timbral brightness, as modeled by SC, and pitch height/ visual brightness/ numerical value processing are semantically congruent and incongruent. 

In four online experiments varying in priming strategy, onset timing, and response deadline, 189 total participants were presented with a baseline stimulus (a pitch, gray square, or numeral) then asked to quickly identify a target stimulus that is higher/ lower, brighter/ darker, or greater/ less than the baseline after being primed with a bright or dark synthetic harmonic tone (see below). Additionally, in the pitch and visual tasks, a deceptive same-target condition was included. Each experiment involved two baseline stimuli and thus a total of four targets (two per baseline). <br clear="right"/>

<img src="/assets/img/projects/app_exp_sounds.png" alt="audio stimuli" align="right" width="300"/> Audio stimuli were additive harmonic complexes up to 10 kHz. We used two baseline F0 values seven semitones or a perfect fifth apart, namely E♭4 and B♭4 (see image on the right). Each baseline was paired with a target two semitones up (F4 and C5, respectively) and a target two semitones down (D♭4 and A♭4, respectively). 

Visual stimuli included two baseline images each comprising a gray square (640 × 640 pixels) with 40% and 60% opacity, respectively. For numerical stimuli, we used two baseline digits: 4 and 7. Each baseline was paired with one larger (+ 2) and one smaller (− 2) digit. <br clear="right"/>

**Bird’s-eye view:** We found that timbral brightness modulates the perception of pitch and visual brightness, but not numerical value. 

**Intramodal interference: Pitch height and timbral brightness** - Semantically incongruent pitch height-timbral brightness shifts produced significantly slower choice reaction time and higher error compared to congruent pairs; timbral brightness also had a strong biasing effect in the same-target condition (i.e., people heard the same pitch as higher when the target tone was timbrally brighter than the baseline, and vice versa with darker tones). 

**Crossmodal interference: Visual brightness** - In the visual task, incongruent pairings of grey squares and tones elicited slower choice reaction times than congruent pairings. We found significant visual * timbral brightness interactions in Exp. 1 & 3, but non-significant interactions in Exp. 2 & 4, and no effect on response accuracy

**Amodal interference: Numerical value** - No interference was observed in the exploratory number comparison task in Exp. 1 & 2. 

Evidence of timbre possibly modulating visual brightness but not numerical value lends support to the crossmodal connectivity hypothesis (direct connectivity between auditory and other sensorimotor channels), although without conclusively ruling out amodal magnitude processing. We are currently following up on these results with a functional magnetic resonance imaging (fMRI) study using modified pitch-brightness and auditory-visual brightness interaction paradigms to investigate the underpinning modulation mechanisms. 
