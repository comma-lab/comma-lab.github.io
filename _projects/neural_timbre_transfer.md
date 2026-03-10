---
layout: page
title: Neural Audio Synthesis and Timbre Transfer
description:
order: 5
redirect: false
display: true
---

<h4>Neural Waveshaping Synthesis</h4>

[Hayes, Saitis, and Fazekas (2021)](https://comma.eecs.qmul.ac.uk/assets/pdf/hayes_neural_2021.pdf) introduced the Neural Waveshaping Unit (NEWT). Before NEWT, the dominant approach to controllable neural audio synthesis was the DDSP autoencoder---powerful, but relying on millions of parameters and often incapable of real-time inference on a plain CPU. NEWT uses a compact bank of multilayer perceptrons with sinusoidal activations to implicitly learn nonlinear waveshaper functions that capture the characteristics of a target instrument timbre. A separate control encoder, conditioned on pitch and loudness, generates time-varying parameters that shift and scale the waveshapers, allowing the model to evolve timbres dynamically across a performance/phrase. The whole architecture, including a differentiable noise synthesiser and learnable reverb, runs on only around 260,000 parameters, more than twenty times fewer than competing methods at the time.

In evaluation against state-of-the-art benchmarks on violin, trumpet, and flute recordings, NEWT performed competitively on FAD (Fréchet Audio Distance) and in a MUSHRA listening test, and outperformed all benchmarks on CPU inference speed. For violin, where high-frequency harmonic energy posed challenges for the shaping functions, performance was slightly weaker than in other experiments. An additional FastNEWT optimisation replaced the learned shaping functions with lookup tables, cutting CPU inference time by nearly a factor of three while maintaining audio quality. 

<h4>Timbre Transfer with VAEs and Cycle-Consistent GANs</h4>

[Sammut Bonnici, Benning, and Saitis (2022)](https://comma.eecs.qmul.ac.uk/assets/pdf/paper_IJCNN_2022.pdf) proposed a VAE-GAN approach to timbre transfer. The main idea, based on the [UNIT image style transfer model](https://proceedings.neurips.cc/paper/2017/file/dc6a6489640ca02b0d42dabeb8e46bb7-Paper.pdf), is that a shared latent space can encode *content* in a timbre-agnostic way, while separate decoders reconstruct audio in the style of different target timbres. The model was trained on mel-spectrograms, with a WaveNet vocoder handling the final conversion back to waveforms. Cycle consistency---encoding in one domain and reconstructing in another, then going back again---provided the self-supervised signal needed to work without paired training data. 

Experiments tested the approach on both voice conversion (using the Flickr 8k Audio dataset) and instrument timbre transfer (using the URMP dataset). Four model variants were compared: the baseline architecture, a version with KL divergence removed from the cyclic loss, a bottleneck residual block design, and a many-to-many extension training across multiple timbres simultaneously. The latter consistently produced the best content reconstruction (as measured by the Structural Similarity Index on mel-spectrograms), confirming that exposing the shared encoder to greater timbral variation helps it learn more general content representations. On the other hand, bottleneck residual blocks reduced the richness of information flowing through the latent space. Adversarial translation quality, measured by FAD on the vocoded audio, was generally better for speech than for instruments, likely due to the comparatively small size of the instrument dataset (cello with the least training data fared worst).

<h4>Interactive differentiable modal resonators</h4>

Physical models of rigid bodies are used for sound synthesis in applications from virtual environments to music production. Traditional methods such as modal synthesis often rely on computationally expensive numerical solvers. [Diaz, Hayes, Saitis, Fazekas, and Sandler (2023)](https://comma.eecs.qmul.ac.uk/assets/pdf/Rigid-Body_Sound_Synthesis_with_Differentiable_Modal_Resonators.pdf) proposed to train a neural network end-to-end to predict the parameters of a differentiable IIR filter bank, where each filter corresponds to a resonant mode. The network takes as input a 2D occupancy grid describing the shape of an object, along with material parameters (density, Young's modulus, Poisson's ratio, damping coefficients) and the position of the excitation point. The frequency-domain sampling method is used during optimisation to sidestep the instability of backpropagating through recursive IIR filters. The results showed that the model closely matched the frequency distributions of FEM (finite element method) synthesised audio for unseen shapes and materials, while running substantially faster: to produce a mesh with 1792 vertices, the FEM solver took slightly over 1.7 seconds, while the proposed method required only 0.08 seconds, falling to around 0.01 seconds if the shape embedding is cached. 

[Diaz, Saitis, and Sandler (2023)](https://nime.org/proceedings/2023/nime2023_81.pdf) demonstrated that the generated filter bank is suitable for a real-time interactive system, implemented as a Max/MSP patch, allowing realistic contact sounds to be produced interactively using a variety of different excitation signals. Material properties can be swept continuously at control rate (1000 Hz), and the network produces smooth coefficient transitions without additional interpolation. Experiments showed that modulating the Young's modulus approximates physically realistic pitch glides after large impacts, while pushing parameters outside the training range produces speculative but musically interesting timbral effects. Click on the image below to see a video showcasing the [Neural Resonator VST](https://github.com/rodrigodzf/NeuralResonatorVST) plugin. See also its [implementation on Bela](https://github.com/rodrigodzf/NeuralResonatorBela).

[![Everything Is AWESOME](https://img.youtube.com/vi/HnUc3VTUReo/0.jpg)](https://www.youtube.com/watch?v=HnUc3VTUReo "Everything Is AWESOME")




