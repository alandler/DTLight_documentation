---
title: Introduction
sidebar: mydoc_sidebar
permalink: mydoc_introduction.html
folder: mydoc
---
{% include note.html content="DTLight is produced for traffic management. You will not have permission to access the tool until explicitly requested and validated." %}

## System Overview

A given intersection is controlled by a meta controller. This is the basis of the entire application.

### 1. Diagram

![Diagram of method](images/method_diagram.png)

### 2. How we use reinforcement learning: state space

We use reinforcement learning to train traffic lights in simulated environments. Based on the state space (shown below), we train a policy that selects how that traffic light should react to the environment.
![A four-way intersection state space.](images/state_space.png)

### 3. Experts as decision trees

Reinforcement learning utilizes a neural network, which is hard to interpret. We use imitation learning to train decision trees that replicate the neural network policy as best they can. The result is binary trees that we call "experts". Each node represents a boolean expression about a given cell. The leaves of the tree denote the action ultimately taken.
![A sample expert.](images/sample_expert.png)

### 4. Metacontrollers

A major innovation of our control scheme is creating a decision tree that determines which expert to use - essentially, a tree of trees. Based on unique factors, such as time of day or presence of emergency vehicles, the traffic light can adapt. It also enables supervision of the system in real time, guaranteeing adequate safety.

![A diagram of metacontroller architecture.](images/metacontroller_diagram.png)

### 5. Supervision:

#### (a) Online 
In real time, our algorithm identifies potentially unsafe situations and passes control to a pre-validated expert. This also logs the occurrence for review.

#### (a) Offline
Logs can be reviewed at any time. The dashboard provides background and footage of the situation such that traffic engineers can determine if they want to permanently alter the RL-based expert to handle the situation.

## Getting started

To get started, see [Getting Started][index].

{% include links.html %}
