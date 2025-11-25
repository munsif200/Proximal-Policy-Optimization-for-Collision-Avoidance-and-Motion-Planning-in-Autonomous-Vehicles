# Proximal Policy Optimization for Collision Avoidance and Motion Planning in Autonomous Vehicles

**A Mathematical Modeling Perspective**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Paper Status](https://img.shields.io/badge/Status-Published-success)](https://www.worldscientific.com/doi/10.1142/S0218348X25401711)

## 📌 Overview

This repository contains the implementation of an end-to-end **Deep Reinforcement Learning (DRL)** framework for autonomous driving, as presented in our paper published in *Fractals (2025)* [4, 7].

Traditional Autonomous Driving Systems (ADS) often struggle with inefficient discrete action spaces. This framework utilizes **Proximal Policy Optimization (PPO)** to enable Autonomous Vehicles (AVs) to perform efficient **Motion Planning and Collision Avoidance (MPCA)** in complex, dynamic environments [25, 26].

---

## 📊 Conference Poster

Below is the official poster for the MMCS 2024 conference.

![MMCS 2024 Conference Poster](./Poster/MMCS-2024_Fractals.pdf)

> **[📄 Download Full Poster as PDF](./Poster/MMCS-2024_Fractals.pdf)**

---

## 🔑 Key Features

* **Multimodal Perception:** Fuses data from **Cameras (RGB), LIDAR, and GPS** for robust state estimation [27, 41].
* **Continuous Control:** Predicts continuous values for **steering angle** ($-25^{\circ}$ to $25^{\circ}$) and **throttle speed** ($0$ to $100~km/h$) rather than discrete actions [227, 230].
* **PPO Optimization:** Utilizes Proximal Policy Optimization for stable convergence, outperforming DQN, A3C, and SAC in our benchmarks [255, 423].
* **Immediate Reward System (IRS):** A custom reward function designed to balance trajectory following with collision avoidance [287].

## 🏗️ System Architecture

The framework operates in an end-to-end manner:

1.  **Observation:** Analyzing 3D surroundings via LIDAR and road visuals via Camera ($84\times84\times3$) [226].
2.  **Learning:** A 7-layer CNN extracts features, fed into a PPO-optimized policy network [216].
3.  **Action:** The network outputs real-time steering and acceleration commands [227].



## 🛠️ Experimental Setup & Prerequisites

The framework was trained and evaluated using the **Unity ML-Agents** toolkit.

| Component | Specification |
| :--- | :--- |
| **Engine** | Unity 2019.3.0 [275] |
| **ML Toolkit** | Unity ML-Agents 0.19.0 [272] |
| **Deep Learning** | TensorFlow 2.0.0 [276] |
| **Inference** | Unity Barracuda [283] |
| **Hardware Used** | NVIDIA GTX 1070, Intel Xeon X5560 [285] |

## 📈 Results

Our PPO-based agent was tested against state-of-the-art baselines (DQN, A3C, SAC) over 5 million simulation steps [322].

* **Accuracy:** Achieved **92% success rate** on structured roads and **84%** on highly complex scenarios with dynamic obstacles [367, 385].
* **Convergence:** Demonstrated superior stability and faster convergence compared to DQN and SAC [551].

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
