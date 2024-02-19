# Goals:

- set the stage
- show I know the literature
- explain the capabilities before
- show what I did
- explain the insight
- explain what it unlocks

# Modalities

- mercredi 28 février 2024 à 15:00 - Salle BC010 - EPFL 1015 Lausanne.
- 40 minutes => 20 content slides, 2 min/slide
- prepare day before
- test run 

# Outline

## Start the work on this in 2019 (joined lions in 2019, almost didn't join)
graphvae first (ICANN)
https://cnrs.hal.science/hal-01990381/
then  molgan (ICML workshop)
https://dare.uva.nl/search?identifier=daa75b2d-d472-45d3-acfd-578dd4e3430f
then condgen
https://proceedings.neurips.cc/paper/2019/hash/e57c6b956a6521b28495f2886ca0977a-Abstract.html
=> october 29 2019 initial meeting
=> condgen fresh state of the art
maybe shared with semi-implicit GVAE https://proceedings.neurips.cc/paper_files/paper/2019/hash/fd4771e85e1f916f239624486bff502d-Abstract.html
## Motivation: Modeling Circuit Netlists


### Slide 1: EDA flow overview

### Slide 2: Why Netlists?
program synthesis
symmetries
need multi-modality anyway
interesting research bit
graph generation
### Slide 3: Mini Overview SotA at 2019

- Google does place & route and other cool neural stuff => we don't do that, no energy to compete w google
- netlists are underdeveloped though (show examplles)

### Slide 4: What we want
(basically the desiderata)

- need to be efficient (samples)
- need to be be efficient (inference,memory)
- need to scalable (stay efficient)

### Slide 5: GNN + Equivaraint overview


## Package 1: Equivariant implicit model GAN

### Slide 6: GG-GAN teaser

fix with latent state positional embeddings
explanation on why it worked:
later on https://proceedings.neurips.cc/paper_files/paper/2022/hash/6d9aac9407bcb1a5957401fa0b8de693-Abstract-Conference.html
https://arxiv.org/abs/2401.01869

### Slide 7: Setting the stage
- graphVAE/VAE=> likelihood based odel
- MolGan https://arxiv.org/pdf/1805.11973.pdf => implicit model, but not PE

### Slide 8: Why does Equivariance matter
discuss clements papers here?  jegelka=
### Slide 9: Collision Problem

### Slide 10: What makes GG-GAN work

- asymmetry => cite the paper
- latent positional embeddings => clement factorizes them
- possible future work: regularize/parametrize for uniqueness (kinda done by clement)

### Slide 11: Summary: what did GG-GAN change/enable

- scale up graph generation
- inspire top-n
- enable SPECTRE
- still more memory efficient model (since generates off of tokens)

## Package 2: Digress + HigenDiff

### Slide 12: 2019, intro of score matching diffusion sde

### Slide 13: Background/explanation around score matching (summary)
- likelihood model that doesn't need to estimate normalizing constant!
### Slide 14: Background Discrete State Spaces
### Slide 15: Digress
### Slide 16: What makes Digress Work

- edges explicitly modeled (no compression)
- empirical noise distribution (convergence of MCMC) (actually done before in a different way  https://arxiv.org/abs/2106.06406)
- discrete state spaces

### Slide 17: How to scale digress 
- recap of louvain
- recap of higendiff

### Slide 18: How to integrate hierarchy into digress

### Slide 19: Comparison to other work

-  mention clementen etc

### Slide 20: Show circuit experiments (evaluation of all 3, do some metrics)


### Backup slides:

TBD tomorrow





