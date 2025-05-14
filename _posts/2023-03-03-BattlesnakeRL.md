---
title: "Reinforcement Learning for Battlesnake"
date: 2023-04-18T15:34:30-04:00
categories:
  - Projects
tags:
  - Cucai Project
  - Previous Club Project
---

UVic AI's primary project is using reinforcement learning to build a top competitor in the game Battlesnake. Battlesnake is an internationally played game in which 4 snakes fight for survival in a digital environment. Each turn, every snake's code is sent the complete state of the environment and given 500ms to compute and submit their next move. To train in this multi-agent synchronous game environment, we have built a modified Monte Carlo Tree Search algorithm that trains via self-play (inspired by AlphaZero). Our current model is at an intermediate level of play and showing no signs of diminishing returns.

Our paper, as it was submitted to CUCAI 2023.

Our future goals are to improve the interpretability of this RL model, to implement Random Network Distillation and other MCTS modifications, and to scale up training until we're first place on the leaderboard.

We also help those with less programming experience write their first battlesnakes using basic heuristics during the lead-up to seasonal Battlesnake tournaments.