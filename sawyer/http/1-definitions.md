---
title: Definitions
nav: true
---

{% include mathjax.html %}

# Reinforcement Learning
<!-- drawn from https://blog.statsbot.co/introduction-to-imitation-learning-32334c3b1e7a -->
{% include figure.html file="reinforcement_learning.png" caption="Reinforcement Learning" src="https://blog.statsbot.co/introduction-to-imitation-learning-32334c3b1e7a" height="7.5cm" %}

In a Reinforcement Learning process the agent gets a reward (positive or negative) for every action he does.
During the training the agent learns how to maximise the reward.

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

# Imitation Learing (or learning by demonstration, programming by example)
Imitation Learning describes the process of training an agent to mimic a certain behaviour.
The agent tries to learn new skills by observing demonstrations of an expert.

The data collected during demonstration is saved in the form of observation-action pairs. <!-- drawn from paper ZERO-SHOT VISUAL IMITATION -->

It is hereby assumed that there is an expert available from whom the agent can learn from.
This means that the agents skills are based on training the experts behaviour and cannot recover from failures in case the demonstration data had imperfections.

## Policy
The goal of Imitation Learning is to find a function that maps the current state to the action.
This function is referred to as **policy**. The success of a policy is measured by means of the total reward that the policy can achieve.

# Attention in Neural Networks
<!-- drawn from http://akosiorek.github.io/ml/2017/10/14/visual-attention.html -->
Informally, a neural attention mechanism equips a neural network with the ability to focus on a subset of its inputs (or features): it selects specific inputs.
There are two main attention mechanisms:
- Hard attention
- Soft attention

# Convolutional Neural Networks
helpful links:
<a href="https://www.youtube.com/watch?v=FmpDIaiMIeA">Youtube - ConvNets</a>

## Softmax Function
<!-- drawn from https://en.wikipedia.org/wiki/Softmax_function -->
The softmax function is a generalization of the logistic function that "squashes" a K-dimensional vector $$ \mathbf {z} $$ of arbitrary real values to a K-dimensional vector $$ \sigma (\mathbf {z} ) $$ of real values, where each entry is in the range $$ (0, 1] $$, and all the entries add up to 1. The function is given by

$$ \sigma (\mathbf {z} )_{j}={\frac {e^{z_{j}}}{\sum _{k=1}^{K}e^{z_{k}}}} $$

In a neural network this is used to squash the output values that indicate the probability into the range of 0 to 1 in a way that they add up to 1. This will make it easier to illustrate the probability of the outcome.

## Cross-Entropy Function
$$ H(p,q)=-\sum _{x}p(x)\,\log q(x) $$

The cross-entropy function is a error function in a neural network that indicates how good the results of the network were.
Other used error functions are e.g. the classification error and the mean squared error.

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
