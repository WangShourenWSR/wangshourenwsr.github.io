---
layout: page
title: Simulation for Sensorimotor Control
description: Use Reinforcement Learning method to demonstrate human Center Nervous System's adaptability 
img: assets/img/projects/sensorimotor_control/1.experiments.png
importance: 2
category: work
related_publications: false
---

## Introduction
This is my first reinforcement learning project, and it is a theoretical tabular reinforcement learning method based project. In this project, I applied a reinforcement learning algorithm, Value-Iteration based Adaptive Dynamic Programming (ADP) to a augmented sensorimotor system to explain the Central Nervous System’s (CNS’s) learning ability and adaptivity to perturbed environment and time delay in limbs' movement. 

## Method
The methodology is based on a <a href="https://link.springer.com/article/10.1007/s00422-014-0613-7"> previous research </a> which models limb's movement as a Linear Time-Invariant (LTI) system and applies Policy-Iteration based Adaptive Dynamic Programming (ADP) to a solve the unknown system dynamic. However, it did not take into account the time delay issues and CNS's adaptability to time delay in sensorimotor control. To address this limitation, in this research, I introduced time delay to the LTI system and applied state-augmentation and Value Iteration based ADP algorithm to demonstrate the Central Nervous System’s (CNS’s) adaptability to time delay in limbs' movement. 
### Modeling
The following is the how we model this scenario and how to introduce time delay.
The experient scenario:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/1.experiments.png" alt="Experiment Scenario" style="width: 20%; height: auto;">
</div>
The system ordinary differential equations:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/2.LTI_system.png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
Introduce time delay to the system:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/3.time_delay.png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>

### Augmentation
Inspired by a <a href="https://ieeexplore.ieee.org/abstract/document/9254117?casa_token=HC05knlZDkAAAAAA:ZXpMeMqXw40jGATdSkpRVhTc0thnTottG6JOxWjanHlI5ufbS8Z8DRopugBRtgqI3hbdm34I">paper for autonomous vehicles</a> and its state augmentation idea I augmented the state vector with past state and control vectors to eliminate the effect of time delay. 
To augment the system with past states and control vectors, we must first discretize the system. The discretization method is:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/4.discretization_and_augmentation.png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
Then, augment the discrete LTI system with past state and control vectors:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/5.augmentation.png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
Subsequently, I applied Value Iteration based ADP algorithm to the augmented LTI system and conducted simulation in a Python environment. The Value Iteration based ADP algorithm is shown as below.
The Value Iteration based ADP is based on Value Iteration algorithm in Dynamic Programming when the system dynamic is known (model-based). Here is the model-based method is shown as below:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(1).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(2).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>

### Adaptive Dynamic Programming
To solve the unknow system dynamic (Matrices A and B), we introduced the Data-Driven method, Value Iteration based ADP to generate the control gain matrix K (policy) from data obtained from the environment instead of the known system dynamic (Matrices A and B).
(In some sense, this approach is similar to Q-learning, where H matrix defines the action-value function:)
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(3).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(4).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(5).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(6).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
By applying ADP, we can obtain the control policy from data instead of system model:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(7).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>
The overall algorithm is: 
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/6.ADP(8).png" alt="Experiment Scenario" style="width: 70%; height: auto;">
</div>

# Results
The simluation result has shown CNS's learning ability and adaptivity to perturbed environment and time delay in limbs' movement.
Human's trajectory during learning:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/7.human_learning.png" alt="Experiment Scenario" style="width: 20%; height: auto;">
</div>
Human's trajectory after learning:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/7.human_post_learning.png" alt="Experiment Scenario" style="width: 20%; height: auto;">
</div>
Model's trajectory during learning:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/7.simulation_learning.png" alt="Experiment Scenario" style="width: 50%; height: auto;">
</div>
Model's trajectory after learning:
<div style="text-align: center;">
  <img src="/assets/img/projects/sensorimotor_control/7.simulation_post_learning.png" alt="Experiment Scenario" style="width: 50%; height: auto;">
</div>


The project is implemented in Python and has not yet been uploaded to GitHub. For access to the project code, please feel free to contact me directly.
