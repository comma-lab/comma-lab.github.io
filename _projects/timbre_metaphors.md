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

Timbre is notoriously difficult to define, and even harder to talk about. Yet people do talk about it, especially musicians, composers, producers, instrument makers, and with surprising consistency. Previous studies have converged on a small number of recurring semantic dimensions, which can be interpreted broadly in terms of brightness/sharpness (or luminance), roughness/harshness (or texture), and fullness/richness (or mass). Read a comprehensive review of the field [here](/assets/pdf/Saitis_chap5.pdf).

These semantic descriptions of timbre embody conceptual representations, allowing listeners to talk about subtle acoustic variations through other, more commonly shared corporeal experiences---*metaphors we listen with*. The [luminance-texture-mass (LTM) model](https://joshreiss.github.io/documents/2014/Zacharakis%20Pastiadis%20Reiss%20-%20Music%20Perception.pdf) describes how listeners across different languages tend to reach for the same kinds of metaphor. 

But how far does this model stretch? And does the way we *talk* about timbre actually track how we *make* sounds?

<h4>Disembodied Timbres</h4>

Most of what we know about what is called "timbre semantics" comes from studies using acoustic orchestral instruments. [Hayes, Saitis, and Fazekas (2022a)](https://drive.google.com/file/d/1E3OV8WdJnNkkFwDu_pzpIjt-R6ml9qV2/view) asked whether the same conceptual vocabulary applies to sounds with no recognisable physical source: the "disembodied" timbres of electronic synthesis. In a novel experimental paradigm, experienced sound designers programmed an FM synthesiser in response to semantic prompts, and provided semantic ratings on the sounds they created. 

<div style="display: flex; gap: 2rem; align-items: flex-start;">

<div style="flex: 1;">

Your text goes here. It will sit to the left of the video and wrap
naturally as needed. You can write as much as you like and it will
stay aligned with the video on the right.

</div>

<div style="flex-shrink: 0;">
  <video width="320" controls>
    <source src="{{ '/assets/vid/disembodied_interface.mov' | relative_url }}" type="video/quicktime">
  </video>
</div>

</div>


We collected 1,407,604 publicly available posts from a popular synth forum, and looked for adjectives co-occuring with the terms *sound*, *sounding*, *tone*, and *timbre*. An initial list of 96,277 adjectives were independently pruned by two raters down to a list of 27 semantic scales, including "bright," "thick" and "rough" selected as synthesis prompts.


**Exploratory factor analysis of the semantic ratings recovered five dimensions.** The first two broadly echoed the LTM model: luminance and texture merged into a single "sharpness" factor, while mass appeared as a second independent factor. Three additional dimensions emerged, namely clarity, percussiveness, and rawness, which appear to reflect specific qualities of FM timbres that listeners discriminated. 


**Semantic prompts left measurable imprints on synthesiser controls.** Participants tuning for "brightness" and "roughness" made similar adjustments to the modulator parameters, the FM settings that govern the distribution of spectral energy, consistent with the acoustic correlates observed for these descriptors. "Thickness", by contrast, was pursued through the amplitude envelopes, shaping the sustain and temporal decay of the sound. Word affect also left its mark: adjectives with stronger emotional valence (positive or negative) tended to produce sounds with more energy in the higher frequencies and greater inharmonicity, echoing [earlier findings](https://www.researchgate.net/profile/Zachary-Wallmark-2/publication/334157880_Creating_novel_tones_from_adjectives_An_exploratory_study_using_FM_synthesis/links/5d1b9143299bf1547c92a408/Creating-Novel-Tones-From-Adjectives-An-Exploratory-Study-Using-FM-Synthesis.pdf).

<img src="/assets/img/projects/disembodied_FMparams.png" alt="methodology" width="960"/>

<h4>timbre.fun: A gamified interactive system for crowdsourcing a timbre semantic vocabulary</h4>

[Hayes, Saitis, and Fazekas (2022b)](https://comma.eecs.qmul.ac.uk/assets/pdf/ICA_2022_template_final_ABS-0997.pdf) also developed [timbre.fun](https://timbre.fun/), a gamified web platform where anyone can explore a two-dimensional synthesiser space and tag the sounds they create with semantic prompts mined from synthesis forums. Debuted at the 2021 Edinburgh Science Festival, the platform attracted nearly 800 users from 35 countries, yielding hundreds of tagged sounds. Even with this more casual, diverse sample, the emergent structure of the data aligned meaningfully with prior lab findings: prompts like sharp, bright, and harsh clustered together in synthesis space and in acoustic feature space, consistent with the LTM luminance-texture grouping. Crucially, the emotional arousal level of words — how energising or calming they are — proved to be a reliable predictor of the acoustic character of the sounds that people created. Prompt arousal, more than valence or dominance, organised the timbral choices of lay participants and experts alike.
