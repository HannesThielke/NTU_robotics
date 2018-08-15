---
title: Papers
nav: true
---

{% include mathjax.html %}

# Paper Summary: One-Shot Imitation Learning
Paper: [here](files/DUAN-One-Shot Imitaion Learning.pdf)

## Introduction
When programming a robot to learn new tasks, you are facing two main problems:
- **Dexterity**:
- **Communication**:

To overcome these problems, demonstrations should help the robot to abstract the task to a wide range of different starting points.

The robot should learn how to solve a problem on its own without the use of feature engineering or or long training.

Traditional Imitation Learning use policies that ar task-specific. The aim of the One-Shot Imitation Learning is to solve different tasks without having to train the robot for each specific task. The network should be able to solve unseen but related tasks by abstracting the knowledge from the trained task.

## Related work

## One Shot Imitation Learning

### Problem Formalization
Definitions:
- $$ \mathbb{T} $$: Distribution of tasks
- $$ t \sim \mathbb{T} $$: Individual task
- $$ \mathbb{D}(t) $$: Distribution of demonstrations for the task $$t$$
- $$ \pi_\theta (a \mid o,d) $$: A policy
- $$ a $$: Action
- $$ o $$: Observation 
- $$ d \sim \mathbb{D}(t); d = [(o_1, a_1),(o_2, a_2), ..., (o_T, a_T)]$$: Demonstration
- $$ \theta $$: Parameters of the policy
- $$ R_t(d) $$: Scalar-valued evaluation fuction (e.g. a binary value indicating success)

### Block Stacking Tasks

### Algorithm
Behavioral Cloning and DAGGER are used to train the neural network policy

## Architecture
