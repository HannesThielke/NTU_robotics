---
title: Definitions
nav: true
---

{% include mathjax.html %}

# Reinforcement Learning
<!-- drawn from https://blog.statsbot.co/introduction-to-imitation-learning-32334c3b1e7a -->
A reinforcement learning framework can be described as a Markov Decision Process:

$$ \langle S,A,R,T,\gamma \rangle $$

where
- S is the set of states
- A is the set of actions
- R is the reward function $$R(s,a):S \times A \rightarrow \mathbb{R}$$
- T is the transit function $$ T(s,a,s')=p(s' \mid a,s) $$
- $$\gamma$$ is the discounting factor that trades off the balance between the immediate reward and the future reward

Policy function:

$$\pi(s):S \rightarrow A$$

Further links:

- <a href="http://amunategui.github.io/reinforcement-learning/">Amunategui.github.io</a>
- <a href="https://www.youtube.com/watch?v=nSxaG_Kjw_w">Video about Reinforcement Learning</a>&nbsp;

# Imitation Learing
<!-- drawn from one-shot-learning paper -->
Imitation learning considers the problem of acquiring skills from observing demonstrations.

# Attention in Neural Networks
<!-- drawn from http://akosiorek.github.io/ml/2017/10/14/visual-attention.html -->
Informally, a neural attention mechanism equips a neural network with the ability to focus on a subset of its inputs (or features): it selects specific inputs.
There are two main attention mechanisms:
- Hard attention
- Soft attention

# Convolutional Neural Networks
helpful links:
<a href="https://www.youtube.com/watch?v=FmpDIaiMIeA">Youtube - ConvNets</a>

## Dilated Convolutions
<!-- drawn from https://www.youtube.com/watch?v=cGkjH_c4SwI -->
{% include figure.html file="one-shot_imitator_training.png" caption="Regular Convolution vs. Dilated Convolution" height="5.5cm" %}

# Multilayer perceptron MLP
vanilla neural network

# Dataset Aggregation DAGGER
The [DAGGER Algorithm](files/a_reduction_of_imitation_learning_and_structured_prediction.pdf) can be used to train a policy.



<!---
{% include figure.html file="topless_configuration/topless_step_17.jpg" height="6.5cm" %}
&nbsp;
-->
<!--  This table was created with http://tableizer.journalistopia.com 
<figure>
{% include table_style.html %}
<table class="tableizer-table"  cellspacing="0">
<thead><tr class="tableizer-firstrow"><th>Radiometric Units</th><th>Symbol</th><th>Unit</th><th>Photometric Units</th><th>Symbol</th><th>Unit</th><th>Description</th></tr></thead><tbody>
 <tr><td>Radiant power</td><td>$$P$$</td><td>Watts [W]</td><td>Luminous flux</td><td>$$F$$</td><td>Lumens [lm]</td><td>total perceived power of light</td></tr>
 <tr><td>Radiant intensity</td><td>$$I$$</td><td>Watts per steradian [W/ster]</td><td>Luminous intensity</td><td>$$I_v$$</td><td>Candelas [cd = lm/ster]</td><td>perceived power emitted by a light source in a particular direction per unit solid angle</td></tr>
 <tr><td>Irradiance</td><td>$$E$$</td><td>Watts per square metre [W/m2]</td><td>Illuminance</td><td>$$E_v$$</td><td>Lux [lx = lm/m2]</td><td>total luminous flux incident on a surface, per unit area</td></tr>
</tbody></table>
</figure>
<figcaption>Overview of important optical quantities <a href="">(source)</a></figcaption>

<br>

-->
