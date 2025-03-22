---
layout: page
title: A Two-Tier DRL and LLM-Based Agent System for Enhancing Fighting Game Enjoyability
description: Developing a two-tier agent (TTA) system that enhances player enjoyment in Street Fighter II using deep reinforcement learning (DRL) and a Large Language Model Hyper-Agent, which dynamically selects suitable DRL opponents based on player data and feedback.
img: assets/img/projects/sfai/cover.png
importance: 1
category: work
related_publications: false
---
To enhance your enjoyment, let's start with a video!

(In this clip, the player in grey is the deep reinforcement learning agent, while the player in white is a human player.)
<video controls width="640" height="360">
    <source src="{{ site.baseurl }}/assets/video/projects/sfai/game_play_video.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

## Abstract
Deep reinforcement learning (DRL) has effectively enhanced gameplay experiences and game design across various game genres. However, few studies on fighting game agents have focused explicitly on enhancing player enjoyment, a critical factor for both developers and players. To address this gap and establish a practical baseline for designing enjoyability-focused agents, we propose a two-tier agent (TTA) system and conducted experiments in the classic fighting game Street Fighter II. The first tier of TTA employs a task-oriented network architecture, modularized reward functions, and hybrid training to produce diverse and skilled DRL agents. In the second tier of TTA, a Large Language Model Hyper-Agent, leveraging players' playing data and feedback, dynamically selects suitable DRL opponents. In addition, we investigate and model several key factors that affect the enjoyability of the opponent. The experiments demonstrate improvements from 218.56\% to 472.55\% in the execution of advanced skills over baseline methods. The trained agents also exhibit distinct game-playing styles. Additionally, we conducted a small-scale user study, and the overall enjoyment in the player's feedback validates the effectiveness of our TTA system.
**(The content below is outdated and will be updated in the coming weeks.)**


## Introduction
This project focuses on developing a Deep Reinforcement Learning (DRL)-based game-playing agent for Street Fighter II (SF2), with an emphasis on enhancing the agent's enjoyability for players. Conducted as part of my research internship at <a href="https://game.engineering.nyu.edu/"> NYU Game Innovation Lab </a>  under the guidance of Prof. <a href="https://engineering.nyu.edu/faculty/julian-togelius"> Julian Togelius </a>,  in collaboration with <a href="https://jiangzehua.github.io/"> Zehua Jiang </a>, <a href="https://github.com/fernandomsilva"> Fernando Silva </a>, and <a href="https://github.com/smearle"> Sam Earle </a>, the project explores advanced training techniques, such as self-play and reward design, to create an engaging and adaptive game-playing agent to improve players' enjoyment.

## Method
### Initial Challenges
The project began by investigating existing baselines for SF2 DRL agents. The <a href="https://onlinelibrary.wiley.com/doi/full/10.1002/aisy.202300335">first baseline </a> lacked accessible code or a GitHub repository, while <a href="https://github.com/linyiLYi/street-fighter-ai"> the second </a> was a very simple project with poor agent performance. To improve upon this, I tested various DRL models and extended them using auxiliary objectives to better capture key environmental information. However, the agents still failed to learn advanced strategies, highlighting limitations in the original training methods rather than the model's capacity.

### Advanced Training Techniques 
#### Hybrid Self-Play
Inspired by successful self-play pipelines in <a href="https://ieeexplore.ieee.org/abstract/document/10333204?casa_token=kY63BW4ZR04AAAAA:AddafjhRNrkoG_zlwPpfyfNTRCMtbfSZCidzuRHrf2PZcq2wsO6JoieUunCQvsP6pMv2Q_RW">other game AI research</a>, I integrated a hybrid self-play training approach. In this method:
<ol>
  <li>Self-Play: The agent trains by competing against copies of itself, enabling iterative improvement.</li>
  <li>Built-in AI Opponents:To further enhance training diversity, I incorporated rule-based built-in AI designed by CAPCOM engineers as opponents during self-play.</li>
</ol>
This combination enabled the agent to effectively learn advanced skills and strategies, surpassing the limitations of earlier approaches.

#### Reward Design
To make the agent more enjoyable for players, I designed several reward functions aimed at promoting advanced and diverse behaviors. This involved:
Rewarding advanced strategies, e.g. special moves.
Penalizing repetitive or overly simplistic strategies. The reward design process played a crucial role in guiding the agent toward learning behaviors that align with human players' preferences.

## Results
The results demonstrated significant improvements in the agent’s learning and enjoyability: 
<ol>
  <li>Skill Advancement: The agent successfully learned advanced strategies, showcasing a level of play comparable to CAPCOM’s built-in AI.</li>
  <li>Player Enjoyability: The enhanced reward functions and self-play pipeline resulted in agents that provided more engaging gameplay experiences.</li>
</ol>
 

## Future Work and Dissemination
The research is ongoing, with further efforts directed toward refining training settings and exploring hyper-agent methods to enhance enjoyability further. The work is targeted for submission to ICML 2025 and IEEE CoG 2025. 

## Codebase 
The code is available in this<a href="https://github.com/WangShourenWSR/fighting-game-two-tier-agent-system.git">GitHub repository</a>. The project code is well-structured, should be compatible for other OpenAI Gym or OpenAI Gym Retro-based tasks. Agents' model are currently not provided, due to it requires LFS service.
