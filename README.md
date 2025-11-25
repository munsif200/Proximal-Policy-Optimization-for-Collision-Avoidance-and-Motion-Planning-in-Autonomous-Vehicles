<h1 align="center">Proximal Policy Optimization for Collision Avoidance and Motion Planning in Autonomous Vehicles</h1>

<h3 align="center">A Mathematical Modeling Perspective</h3>

<p align="center">
  <a href="https://creativecommons.org/licenses/by/4.0/"><img src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg" alt="License: CC BY 4.0"></a>
  <a href="https://www.worldscientific.com/doi/10.1142/S0218348X25401711"><img src="https://img.shields.io/badge/Status-Published-success" alt="Paper Status"></a>
  <a href="https://www.worldscientific.com/doi/10.1142/S0218348X25401711"><img src="https://img.shields.io/badge/Journal-Fractals%202025-blue" alt="Journal"></a>
</p>

---

## 📊 Conference Poster

<p align="center">
  <strong>MMCS 2024 Conference Poster</strong>
</p>

<p align="center">
  <img src="Poster/P_MPCA.png" alt="MMCS 2024 Conference Poster" width="100%">
</p>

<p align="center">
  <a href="./Poster/MMCS-2024_Fractals.pdf"><strong>📄 Download Full Poster as PDF</strong></a>
</p>

---

## 📌 Overview

This repository contains the implementation of an end-to-end **Deep Reinforcement Learning (DRL)** framework for autonomous driving, as presented in our paper published in *Fractals (2025)*.

Traditional Autonomous Driving Systems (ADS) often struggle with inefficient discrete action spaces. This framework utilizes **Proximal Policy Optimization (PPO)** to enable Autonomous Vehicles (AVs) to perform efficient **Motion Planning and Collision Avoidance (MPCA)** in complex, dynamic environments.

---

## 🔑 Key Features

| Feature | Description |
| :--- | :--- |
| **Multimodal Perception** | Fuses data from **Cameras (RGB), LIDAR, and GPS** for robust state estimation |
| **Continuous Control** | Predicts continuous values for **steering angle** (−25° to 25°) and **throttle speed** (0 to 100 km/h) |
| **PPO Optimization** | Utilizes Proximal Policy Optimization for stable convergence, outperforming DQN, A3C, and SAC |
| **Immediate Reward System** | A custom reward function designed to balance trajectory following with collision avoidance |

---

## 🏗️ System Architecture

The framework operates in an end-to-end manner:

1. **Observation:** Analyzing 3D surroundings via LIDAR and road visuals via Camera (84×84×3)
2. **Learning:** A 7-layer CNN extracts features, fed into a PPO-optimized policy network
3. **Action:** The network outputs real-time steering and acceleration commands

---

## 🛠️ Experimental Setup & Prerequisites

The framework was trained and evaluated using the **Unity ML-Agents** toolkit.

| Component | Specification |
| :--- | :--- |
| **Engine** | Unity 2019.3.0 |
| **ML Toolkit** | Unity ML-Agents 0.19.0 |
| **Deep Learning** | TensorFlow 2.0.0 |
| **Inference** | Unity Barracuda |
| **Hardware** | NVIDIA GTX 1070, Intel Xeon X5560 |

---

## 📈 Results

Our PPO-based agent was tested against state-of-the-art baselines (DQN, A3C, SAC) over 5 million simulation steps.

| Metric | Performance |
| :--- | :--- |
| **Structured Roads** | 92% success rate |
| **Complex Scenarios** | 84% success rate with dynamic obstacles |
| **Convergence** | Superior stability and faster convergence compared to DQN and SAC |

---

## 📚 Citation

If you use this code or the findings in your research, please cite our paper:

```bibtex
@article{Hijji2025Proximal,
  title={Proximal Policy Optimization for Collision Avoidance and Motion Planning in Autonomous Vehicles: A Mathematical Modeling Perspective},
  author={Hijji, Mohammad and Munsif, Muhammad and Alwakeel, Mohammed and Alwakeel, Ahmed and Aradah, Fahad and Cheikh, Faouzi Alaya and Sajjad, Muhammad and Muhammad, Khan},
  journal={Fractals},
  volume={33},
  pages={2540171},
  year={2025},
  publisher={World Scientific},
  doi={10.1142/S0218348X25401711}
}
```

---

<p align="center">
  <strong>© 2025 | Published in <a href="https://www.worldscientific.com/doi/10.1142/S0218348X25401711">Fractals Journal</a></strong>
</p>
