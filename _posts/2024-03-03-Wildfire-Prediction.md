---
title: "Wildfire Prediction"
excerpt_separator: "<!--more-->"
---

Simulating Responsive Action to Wildfire Disasters with Reinforcement Learning (RL)

![Wildfire Management - CUCAI 2024](/assets/images/wildfire_group_img.jpg)


<a href="https://github.com/uvicaiclub/WildfireManagementRL" class="btn btn--primary">
  View GitHub for Code
</a>


## 💖 Motivation
Wildfires are among the most **destructive natural hazards** in Western Canada, contributing significantly to air pollution, ecological damage, and threats to human communities. In British Columbia, annual fire suppression costs are approaching **one billion dollars**, and the scale and intensity of fires continue to increase due to **climate change**.

Developing **intelligent**, **adaptive**, and **cost‑effective wildfire response strategies** is becoming essential. Traditional planning methods struggle to keep pace with the complexity of modern fire behavior, making this an ideal domain for **machine learning research**.

---

## 📝 Background
A variety of fire spread simulators exist today, many of which incorporate **environmental factors** such as:

- Terrain elevation
- Wind speed and direction
- Vegetation and fuel type

These tools are invaluable for **forecasting fire behavior**, but they generally treat the fire as an uncontrolled physical process. Human intervention—arguably the most important variable in real wildfire response—is often missing from the simulation loop.

Previous research has attempted to introduce **reinforcement learning (RL)**nagents into wildfire environments, but these efforts face two major limitations:

- The simulators used are often too simplified to reflect real fire dynamics
- The available agent actions rarely resemble the operational decisions made by actual fire crews

As a result, RL agents may learn strategies that perform well in simulation but fail to translate to real‑world scenarios.

---

## 💡 Our Contributions
Our project seeks to bridge this gap by developing an **RL environment informed by modern fire spread simulators**:

- Parameters of spread dynamics are tuned to reflect **realistic fire behavior in Northwestern BC**  
- **Multiple RL agents** are trained to fight wildfires cooperatively  
- Agent actions are modeled after **actual fire crew operations**, making simulations more realistic and operationally relevant  

---

🔥 This project explores how **AI-driven strategies** could one day assist in minimizing damage, reducing costs, and saving lives during wildfire disasters.
