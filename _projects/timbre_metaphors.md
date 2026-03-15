---
layout: page
title: Metaphors We Listen With
description: 
img: /assets/img/projects/timbrefun_agg.png
order: 1
redirect: false
display: true
---

> *It is a difficult matter to define tone quality in words; we must encroach upon the domain of sight, feeling, and even taste.*<br>— Nikolai Rimsky-Korsakov (1913)

> *A sound’s timbre describes its harshness or softness, its dullness or brightness*.<br>— Jean-Jacques Rousseau (1765)

Timbre is notoriously difficult to define, and even harder to talk about. Yet people do talk about it, especially musicians, composers, producers, instrument makers, and with surprising consistency. Previous studies have converged on a small number of recurring semantic dimensions, which can be interpreted broadly in terms of brightness/sharpness (or luminance), roughness/harshness (or texture), and fullness/richness (or mass). [Saitis and Weinzierl (2019)](/assets/pdf/Saitis_chap5.pdf) provide a comprehensive review of the field.

These semantic descriptions of timbre embody conceptual representations, allowing listeners to talk about subtle acoustic variations through other, more commonly shared corporeal experiences---*metaphors we listen with*. The [luminance-texture-mass (LTM) model](https://joshreiss.github.io/documents/2014/Zacharakis%20Pastiadis%20Reiss%20-%20Music%20Perception.pdf) describes how listeners across different languages tend to reach for the same kinds of metaphor. 

But how far does this model stretch? And does the way we *talk* about timbre actually track how we *make* sounds?

<h4>Disembodied Timbres: a study on semantically prompted FM synthesis</h4>

Most of what we know about what is called "timbre semantics" comes from studies using acoustic orchestral instruments. [Hayes, Saitis, and Fazekas (2022a)](https://drive.google.com/file/d/1E3OV8WdJnNkkFwDu_pzpIjt-R6ml9qV2/view) asked whether the same conceptual vocabulary applies to sounds with no recognisable physical source: the "disembodied" timbres of digital synthesis. 

In a novel experimental paradigm, experienced sound designers programmed an FM synthesiser in response to semantic prompts, and provided semantic ratings on the sounds they created. We collected 1,407,604 publicly available posts from a popular synth forum, and looked for adjectives co-occuring with the terms *sound*, *sounding*, *tone*, and *timbre*. An initial list of 96,277 adjectives were independently pruned by two raters down to a list of 27 semantic scales, including "bright," "thick" and "rough" selected as synthesis prompts.

<video width="700" controls>
    <source src="/assets/vid/disembodied_interface.mp4" type="video/mp4">
</video>
<br/>

**Exploratory factor analysis of the semantic ratings recovered five dimensions.** The first two broadly echoed the LTM model: luminance and texture merged into a single "sharpness" factor, while mass appeared as a second independent factor. Three additional dimensions emerged, namely clarity, percussiveness, and rawness, which appear to reflect specific qualities of FM timbres that listeners discriminated. 

**Semantic prompts left measurable imprints on synthesiser controls.** Participants tuning for "brightness" and "roughness" made similar adjustments to the modulator parameters, the FM settings that govern the distribution of spectral energy, consistent with the acoustic correlates observed for these descriptors. "Thickness", by contrast, was pursued through the amplitude envelopes, shaping the sustain and temporal decay of the sound. Word affect also left its mark: adjectives with stronger emotional valence (positive or negative) tended to produce sounds with more energy in the higher frequencies and greater inharmonicity, echoing [earlier findings](https://www.researchgate.net/profile/Zachary-Wallmark-2/publication/334157880_Creating_novel_tones_from_adjectives_An_exploratory_study_using_FM_synthesis/links/5d1b9143299bf1547c92a408/Creating-Novel-Tones-From-Adjectives-An-Exploratory-Study-Using-FM-Synthesis.pdf).

<img src="/assets/img/projects/disembodied_FMparams.png" alt="methodology" width="900"/>

* Spearman’s *ρ* correlations
* *: *p* < 0.05; **: *p* < 0.01; ***: *p* < 0.001
* F = factor, A = attack; D = decay; S = sustain; R = release; T = tuning; V = volume; 1 = carrier; 2 & 3 = modulators
<br/>

<h4>timbre.fun: A gamified interactive system for crowdsourcing a timbre semantic vocabulary</h4>

Based on the prompted synthesis tasks, [Hayes, Saitis, and Fazekas (2022b)](https://comma.eecs.qmul.ac.uk/assets/pdf/ICA_2022_template_final_ABS-0997.pdf) developed [timbre.fun](https://timbre.fun/), a gamified web platform where anyone can explore a two-dimensional synthesiser space and tag the sounds they create with semantic prompts mined from synthesis forums. Debuted at the 2021 Edinburgh Science Festival, the platform attracted nearly 800 users from 35 countries, yielding hundreds of tagged sounds. Even with this more casual, diverse sample, the emergent structure of the data aligned meaningfully with prior lab findings: prompts like sharp, bright, and harsh clustered together in synthesis space and in acoustic feature space---PCA and k-means clustering on audio features revealed two distinct spaces, consistent with the LTM luminance-texture grouping. 

<img src="/assets/img/projects/timbre_fun_descriptors.png" alt="descriptors in synthesis space" width="750"/>

<img src="/assets/img/projects/timbre_fun_clusters.png" alt="descriptors in audio feature space" width="900"/>

* cluster 1: more energy in low frequencies, and clear peaks in the spectrum 
* cluster 2: a flatter spectrum with more high frequency energy

Very interestingly, **the emotional arousal connotation of timbral metaphors proved to be a reliable predictor of the acoustic character of the sounds that people created.** Using published [word affect norms](https://link.springer.com/content/pdf/10.3758/s13428-012-0314-x.pdf), valence, arousal, and dominance scores were obtained for each prompt. Each affect dimension was treated as a binary classification problem, fitting an SVM (RBF kernel) on either acoustic principal components or synthesiser parameters as input. A binomial test using the no-information rate as the null hypothesis suggested the result for arousal was statistically significant (accuracy: synth parameters 73.1%, acoustic PCs 71%; *p* < 0.001).

<h4>Timbre semantic associations vary both between and within instruments</h4>

<h5>An empirical study incorporating register and pitch height</h5>

[Reymore, Noble, Saitis, Traube, and Walmark (2023)](https://www.mcgill.ca/mpcl/files/mpcl/reymore_2023_muspercept.pdf) looked at the variations in timbre within an instrument and between different instruments, and the corresponding semantic associations. These variations depend on dynamics, pitch, articulation, duration, vibrato, technique, and other parameters. Register-dependent descriptions of instruments’ timbres characterize instruments based on register, or a part of the instrument’s range, such as the rumbling, thick, and muddy low notes of the piano versus the tinkling, thin, and clear highest notes. This relationship is further complicated by the varying tessituras, or range of playable notes, for different instruments (for example, the flute’s lowest notes overlap with the bassoon’s highest notes, as shown below).

<img src="/assets/img/projects/mus_percept_design.png" alt="methodology" align="right" width="650"/> To address these variations, we designed an experiment to examine the effect of register on instrumental timbre semantics, with additional analysis relating specifically to pitch height. Four of the instruments (violin, bass clarinet, trombone, and vibraphone) were selected based on the [ACTOR CORE (Composer-Performer Orchestration Research Ensemble).](https://timbreandorchestration.org/research-ensembles) Vibraphone sounds were bowed, rather than struck, to maintain consistency of excitation type. We then added flute, oboe, trumpet, and cello in order to balance the range of the stimuli and to maximize the variability of orchestral timbres tested. We note that the vibraphone was included precisely because it is an outlier---the only percussion instrument, idiophone, non-default technique, and non-standard orchestral member, offering useful variability for studying how instrument type interacts with register-semantic relationships. <br clear="right"/>

Semantic scales (Reymore and Huron 2020):
| deep, thick, heavy | brassy, metallic | woody |
| smooth, singing, sweet | raspy, grainy, gravelly | muted, veiled |
| project, commanding, powerful | ringing, long decay | sustained, even |
| nasal, buzzy, pinched | sparkling, brilliant, bright | open |
| shrill, harsh, noisy | airy, breathy | focused, compact |
| percussive (sharp beginning) | resonant, vibrant | watery, fluid |
| pure, clear, clean | hollow |
