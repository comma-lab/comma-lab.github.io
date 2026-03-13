---
layout: page
title: Brightness Perception of Musical Sounds
img: /assets/img/projects/strauss_spectrogram_kai.png
order: 10
redirect: false
display: true
---

<img src="/assets/img/projects/bright_sounds.png" alt="spectrograms of four instruments" align="right" width="500"/> Timbre is commonly described using vision terms. Auditory brightness is among the most studied “[metaphors we listen with](/projects/timbre_metaphors/)” and arguably among the most important musical cues actively shaped by performers, composers, and audio engineers. Psychoacoustically, sounds described as ”bright” vs “dull” or ”dark” typically exhibit a high vs low frequency emphasis in the spectrum (see side figure with spectrograms of four acoustic instrument notes, f0 = 311 Hz, 500 ms, mezzo-forte, left channels, loudness matched). However, relatively little is known about the perceptual and neurocognitive mechanisms that facilitate using a visual quality to talk about something that sounds. The following studies set out to explore related questions. <br clear="left"/>

<h4>Relation to timbre dissimilarity and source-cause categories</h4>

Timbre dissimilarity of orchestral sounds is well-known to be multidimensional, with attack time and spectral centroid representing its two most robust acoustical correlates. The centroid dimension is traditionally considered as reflecting timbral brightness. In this study, we posed three important, yet unexplored questions: 
* the first question concerned the dimensionality of brightness as an attribute of timbre. Specifically, we wondered about the dimensionality that timbral brightness would exhibit as an auditory attribute in and of itself if considered through the empirical angle of pairwise dissimilarity ratings of a set of sounds.
* The second related question concerned the robustness (or stability) of brightness judgments across different tasks. Specifically, we wondered about the extent to which direct brightness ratings of a set of sounds would recover their ordering along the SC dimension obtained from general timbre dissimilarity ratings of the same sounds.
* The third question concerned the relation of brightness to source-cause categories. Specifically, we wondered whether brightness dissimilarity ratings of instrumental sounds would be affected by categorical stimulus features related to instrument family membership and the type of resonator and excitation.

A triangulation approach was used to examine the dimensionality of timbral brightness, its robustness across different psychoacoustical contexts, and relation to perception of the sounds' source-cause. Listeners compared 14 acoustic instrument sounds in three distinct tasks that collected general dissimilarity, brightness dissimilarity, and direct multi-stimulus brightness ratings. For the latter, we adapted the MUSHRA procedure (ITU-R BS.1534-3), whereby listeners are allowed to switch between multiple stimuli presented in parallel as often as they want, effectively performing a direct rating of each stimulus plus a ranking and inherently also pairwise comparisons. 

<img src="/assets/img/projects/jasa2020_exp_design.png" alt="methodology" width="420"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="/assets/img/projects/jasa2020_mushra.png" alt="mushra direct brightness ratings" width="420"/>

**Multidimensional scaling**

Dissimilarity ratings were first analysed with nonmetric MDS. The 2D MDS solution for brightness dissimilarity (BRdissim) was compared with a general timbre dissimilarity space (GEdissim). The first dimension of BRdissim reflected spectral envelope organisation, mirroring the second dimension of GEdissim, while its second dimension appeared to reflect temporal envelope structure, with an unexpected placement of the bowed cello. Log attack time (LAT) and spectral centroid (SC) were used as confirmatory descriptors to examine how well they predicted both general and brightness dissimilarity dimensions: SC correlations were as expected; somewhat suprisingly, the second dimension of BRdissim correlated well with LAT. This finding could suggest a leakage of general timbre dissimilarity into timbral brightness dissimilarity, which, like source-cause categories (see below), may further relate to the susceptibility of pairwise dissimilarity ratings to conflate other processes.

<img src="/assets/img/projects/jasa2020_spaces.png" alt="multidimensional scaling" width="420"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="/assets/img/projects/jasa2020_plsr.png" alt="partial least squares regression" width="420"/><br><br>

**Partial least-squares regression**

PLSR models were used to predict GEdissim and BRdissim ratings from acoustic descriptors, source-cause categorical predictors (resonator type, excitation type, instrument family), and their combination. For GEdissim, the acoustic model explained 85% of variance, with one notable outlier (vibraphone-marimba) highlighting the role of categorical cues. The categorical model alone explained 63%, and combining both improved fit significantly. For BRdissim, the acoustic model performed equally well (85%), but categorical predictors were much weaker (40% variance explained), and adding them to the acoustic model yielded no meaningful improvement. These observations were further confirmed by bootstrapped R2 values.

These results replicate [earlier findings](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2015.01977/full) that musicians incorporate source-cause knowledge in general dissimilarity judgements, but show this effect disappears when listeners focus specifically on brightness — suggesting brightness is driven by acoustical rather than causal similarity. Disentangling spectral and temporal contributions to brightness perception would require synthetic stimuli with carefully dissociated properties. 



<h4>Timbral brightness perception investigated through multimodal interference</h4>

Triangulating three different interaction paradigms, we investigated using speeded classification whether intramodal, crossmodal, and amodal interference occurs when timbral brightness, as modeled by the centroid of the spectral envelope, and pitch height/visual brightness/numerical value processing are semantically congruent and incongruent. In four online experiments varying in priming strategy, onset timing, and response deadline, 189 total participants were presented with a baseline stimulus (a pitch, gray square, or numeral) then asked to quickly identify a target stimulus that is higher/lower, brighter/darker, or greater/less than the baseline after being primed with a bright or dark synthetic harmonic tone (left image below). Additionally, in the pitch and visual tasks, a deceptive same-target condition was included. 

Each experiment involved two baseline stimuli and thus a total of four targets (two per baseline). Audio stimuli were additive harmonic complexes up to 10 kHz. We used two baseline F0 values seven semitones or a perfect fifth apart, namely E♭4 and B♭4 (right image below). Each baseline was paired with a target two semitones up (F4 and C5, respectively) and a target two semitones down (D♭4 and A♭4, respectively). Visual stimuli included two baseline images each comprising a gray square (640 × 640 pixels) with 40% and 60% opacity, respectively. For numerical stimuli, we used two baseline digits: 4 and 7. Each baseline was paired with one larger (+ 2) and one smaller (− 2) digit. 

<img style="border:2px solid #555" src="/assets/img/projects/app_exp_design.png" alt="methodology" width="400"/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="/assets/img/projects/app_exp_sounds.png" alt="stimuli" width="400"/><br><br>


**Bird’s-eye view:**

We found that timbral brightness modulates the perception of pitch and visual brightness, but not numerical value. 

**Intramodal interference: Pitch height and timbral brightness**

Semantically incongruent pitch height-timbral brightness shifts produced significantly slower choice reaction time and higher error compared to congruent pairs; timbral brightness also had a strong biasing effect in the same-target condition (i.e., people heard the same pitch as higher when the target tone was timbrally brighter than the baseline, and vice versa with darker tones). 

* Timbral brightness affects pitch height comparisons (Exp. 1)
  * RT: 𝜒2 = 67.5, p < .0001; accuracy: 𝜒2 = 199.4, p < .0001

* Pitch height differences affect timbral brightness comparisons (Exp. 4)
  * RT: 𝜒2 = 34.8, p < .0001; accuracy: 𝜒2 = 166.7, p < .0001 

**Crossmodal interference: Visual brightness**

In the visual task, incongruent pairings of gray squares and tones elicited slower choice reaction times than congruent pairings. 

* Visual * timbral brightness interactions in Exp. 1 & 3, respectively
  * RT: 𝜒2 = 4.73, p = .03; and 𝜒2 = 10.5, p = .001

* Non-significant interactions in Exp. 2 & 4; no effect on response accuracy

**Amodal interference: Numerical value**

No interference was observed in the number comparison task in Exp. 1 & 2. 

Taken together, the present findings broaden our understanding of the cognitive linguistics of timbre and the multimodal interactions that can accompany auditory experience. Evidence of timbre possibly modulating visual brightness but not numerical value lends support to the crossmodal connectivity hypothesis (direct connectivity between auditory and other sensorimotor channels), although without conclusively ruling out amodal magnitude processing. We are currently following up on these results with a functional magnetic resonance imaging (fMRI) study using modified pitch-brightness and auditory-visual brightness interaction paradigms to investigate the underpinning modulation mechanisms. 

Read the full paper [here](https://link.springer.com/article/10.3758/s13414-024-02934-2).
