---
layout: page
title: Interactive Neural Resonators
description: PhD research Rodrigo Diaz
img: /assets/img/projects/gui2.png
order: 5
redirect: false
display: true
---

Physical models of rigid bodies are used for sound synthesis in applications from virtual environments to music production. Traditional methods such as modal synthesis often rely on computationally expensive numerical solvers. 

[Diaz, Hayes, Saitis, Fazekas, and Sandler (2023)](https://comma.eecs.qmul.ac.uk/assets/pdf/Rigid-Body_Sound_Synthesis_with_Differentiable_Modal_Resonators.pdf) proposed to train a neural network end-to-end to predict the parameters of a differentiable IIR filter bank, where each filter corresponds to a resonant mode. The network takes as input a 2D occupancy grid describing the shape of an object, along with material parameters (density, Young's modulus, Poisson's ratio, damping coefficients) and the position of the excitation point. The frequency-domain sampling method is used during optimisation to sidestep the instability of backpropagating through recursive IIR filters. 

The results showed that the model closely matched the frequency distributions of FEM (finite element method) synthesised audio for unseen shapes and materials, while running substantially faster: to produce a mesh with 1792 vertices, the FEM solver took slightly over 1.7 seconds, while the proposed method required only 0.08 seconds, falling to around 0.01 seconds if the shape embedding is cached. 

[Diaz, Saitis, and Sandler (2023)](https://nime.org/proceedings/2023/nime2023_81.pdf) demonstrated that the generated filter bank is suitable for a real-time interactive system, implemented as a Max/MSP patch, allowing realistic contact sounds to be produced interactively using a variety of different excitation signals. Material properties can be swept continuously at control rate (1000 Hz), and the network produces smooth coefficient transitions without additional interpolation. Experiments showed that modulating the Young's modulus approximates physically realistic pitch glides after large impacts, while pushing parameters outside the training range produces speculative but musically interesting timbral effects. 

Click on the image below to see a video showcasing the [Neural Resonator VST](https://github.com/rodrigodzf/NeuralResonatorVST) plugin. See also its [implementation on Bela](https://github.com/rodrigodzf/NeuralResonatorBela).

[![Neural Resonator VST](https://img.youtube.com/vi/HnUc3VTUReo/0.jpg)](https://www.youtube.com/watch?v=HnUc3VTUReo "Neural Resonator VST")




