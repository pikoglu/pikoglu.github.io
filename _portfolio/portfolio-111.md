---
title: "KAMATE – Rugby Board Game Adaptation with AI Opponent"
excerpt: "<img src='/images/portfolio/kamate.png'>"
collection: portfolio
category: Game Projects
---

* __With__: [François Gourgue](https://github.com/FrancoisGourgue), [Erwan Estève](https://github.com/ErwannE), [Vianney de Monicault](https://github.com/LempereurV)  
* __Resources__: [Code](https://github.com/LempereurV/KAHMATE) 
* __When__: 2024  
* __Associated to__: TDLog – Software Engineering Practices

KAMATE is a digital adaptation of a lesser-known rugby-themed board game, built from scratch using Python and a 2D game development library ( [Pygame](https://www.pygame.org/news)). The goal was to replicate the core gameplay mechanics in a digital environment while keeeping to solid software engineering principles, as part of the TDLog course.

The game includes all major features from the physical version:  
– Turn-based mechanics  
– Player movement, tackling, ball handling  
– Full game rules implementation for 1v1 matches

To enhance the solo experience, we developed an AI opponent using reinforcement learning. Two agents were implemented and compared:

- **Epsilon-Greedy Strategy**: A baseline agent using a heuristic-driven decision policy, balancing exploration and exploitation with a decaying epsilon schedule.
- **Q-Learning Agent**: A state-based reinforcement learning agent that learned optimal actions through self-play. The state space was simplified using feature extraction techniques (e.g., distance to goal, ball possession, proximity to opponents), and the action-value function was stored in a lookup table updated over multiple training episodes.

KAMATE was an opportunity to combine game design, AI, and collaborative software development in a constrained yet meaningful real-world setting.
