---
title: Papers
nav: true
---

{% include mathjax.html %}

# Paper Summary: One-Shot Imitation Learning
Paper: [here](files/one-shot_imitaion_learning.pdf)

## Introduction
When programming a robot to learn new tasks, you are facing two main problems:
- **Dexterity**: The robot has to learn how to complete difficult tasks in right way
- **Communication**: When telling the robot what to do, it has to understand the general meaning of the instruction to adapt it to a broader set of tasks

To overcome these problems, demonstrations should help the robot to abstract the task to a wide range of different starting points.
Unlike traditional Imitation Learning techniques the aim of the One-Shot Imitation Learning is to train one policy to solve unseen tasks that are similar to the demonstrated sample task. 
The robot should learn how to solve a problem on its own without the use of feature engineering or or long training.

<!-- ## Related work -->

## One Shot Imitation Learning
{% include figure.html file="one-shot_imitation_learning.png" caption="One-Shot Imitation Learning" height="5.5cm" %}
{% include figure.html file="one-shot_imitator_training.png" caption="Training the One-Shot Imitator" height="5.5cm" %}

### Problem Formalization
<center><figure>
{% include table_style.html %}
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>Variable</th><th>Description</th></tr></thead><tbody>
 <tr><td>$$ \mathbb{T} $$</td><td>Distribution of tasks</td></tr>
 <tr><td>$$ t \sim \mathbb{T} $$</td><td>Individual task</td></tr>
 <tr><td>$$ \mathbb{D}(t) $$</td><td>Distribution of demonstrations for the task t</td></tr>
 <tr><td>$$ \pi_\theta (a \mid o,d) $$</td><td>A policy</td></tr>
 <tr><td>$$ a $$</td><td>Action</td></tr>
 <tr><td>$$ o $$</td><td>Observation</td></tr>
 <tr><td>$$ d \sim \mathbb{D}(t) $$</td><td>Demonstration $$ d = [(o_1, a_1),(o_2, a_2), ..., (o_T, a_T)]$$</td></tr>
 <tr><td>$$ \theta $$</td><td>Parameters of the policy</td></tr>
 <tr><td>$$ R_t(d) $$</td><td>Scalar-valued evaluation fuction (e.g. a binary value indicating success)</td></tr>
</tbody></table>
</figure></center>
<figcaption>Variables</figcaption>

### Block Stacking Tasks

### Algorithm
Behavioral Cloning and DAGGER are used to train the neural network policy

## Architecture

{% include figure.html file="network_architecture.png" caption="Network architecture" height="8.5cm" %}

The architecture that is used for One-Shot Imitation Learning consists of three modules:
- Demonstration Network
- Context Network
- Manipulation Network

### Demonstration Network
To improve the performance of the policy for long-term demonstration sequences a random number of time steps is discarded during **Temporal Dropout**.
In the next steps the demonstration goes through the process of **Dilated Temporal Convolution** and **Neighbourhood Attention**.
The step of Neighborhood Attention allows every block to query other blocks in relation to itself.

### Context Network
<!-- TODO -->

### Manipulation Network
The manipulation network computes the action of stacking the blocks using an MLP network.

# Paper Summary: Zero-Shot Visual Imitation
Zero-Shot Visual Imitation in this paper is achieved by the following steps.
The training of an agent is done by letting the agent explore the environment without any expert supervision.
All visited states during this exploration are labeled as goals and all actions are labeled as targets.
A "forward consistency loss" function makes sure that the final goal is more important than the steps towards this goal.
In this way it is possible to have different ways to the same solution.

## Learning To Imitate Without Expert Supervision
The data gathered during exploration is used to learn a deep network "goal-conditioned skill policy GSP".
To imitate a given task, the GSP is fed with the image data from the demonstration