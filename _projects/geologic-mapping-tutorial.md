---
name: Geologic Mapping Tutorial
tools: [stanford, gis, education]
image: http://placekitten.com/250/250
description: Wrote a 3-hour tutorial for creating geologic maps using the USGS GEMS framework.
---

## Title of Project ##

![A photo](http://placekitten.com/400/375)

Here, $$\textbf{D}$$ is the dropout *layer* or operator which sets a subset of its input randomly to zero with dropout probability `p`. This modification can be adopted for any other RNN architecture.

*Zaremba et al* used these architectures for their experiments in which each cell was unrolled for 35 steps. Mini-batch size was 20 for both :

**Medium LSTM** :
Hidden-layer dimension = `650`,
Weights initialized uniformly in `[-0.05,0.05]`,
Dropout probability = `0.5`,
Number of epochs = `39`,
Learning rate = `1` which decays by a factor of `1.2` after 6 epochs,
Gradients clipped at `5`.

**Large LSTM** :
Hidden-layer dimension = `1500`,
Weights initialized uniformly in `[-0.04,0.04]`,
Dropout probability = `0.65`,
Number of epochs = `55`,
Learning rate = `1` which decays by a factor of `1.15` after 14 epochs,
Gradients clipped at `10`.
### Result highlights
* 78.4 PPL on Penn TreeBank dataset using a single **Large LSTM**
* 68.7 PPL on Penn TreeBank dataset using an ensemble of 38 **Large LSTM**s

<< [Back to Projects](/projects/)