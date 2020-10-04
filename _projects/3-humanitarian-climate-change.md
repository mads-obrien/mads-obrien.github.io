---
name: Humanitarian Aid & Climate Change
tools: [data analysis, humanitarian, writing, speaking, yale]
image: /myassets/thumbnail_humanitarian.jpg
description: Helped write a paper and presented in Geneva, Switzerland.
---

## Title of Project ##

![A photo](http://placekitten.com/400/375)

We are published!  
> *Accepted, in press.* McCann, B. T., Davis, J., Osborne, D., Durham, C., **O’Brien, M.**, and Raymond, N. A. (2020). Quantifying climate change relevant humanitarian programming and spending across five highly disaster vulnerable countries. *Disasters.* [doi.org/10.1111/disa.12453](https://doi.org/10.1111/disa.12453)

{% include elements/button.html link="https://onlinelibrary.wiley.com/doi/epdf/10.1111/disa.12453" text="View accepted article" style="primary" size="sm" %}
{% include elements/button.html link="https://reliefweb.int/report/syrian-arab-republic/quantifying-climate-change-relevant-humanitarian-programming-and" text="View on ReliefWeb" style="primary" size="sm" %}

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