# IS_597_Project
Final Project for IS597

# Autonomous Vehicle Sensor Simulation using Monte Carlo Methods

## Overview

This project uses Monte Carlo simulations to simulate autonomous vehicle sensor systems and their performance under variable driving and environmental conditions. It provides a modular framework to model, simulate, and analyze the behavior of key perception sensors—camera, LiDAR, and Radar—in diverse traffic and weather conditions.

The primary goal is to assess system robustness, sensor reliability, and detection accuracy under uncertainty, thereby supporting the development of safer and more resilient autonomous navigation strategies.

---

## Features

- 🧠 **Sensor Abstractions**: Modular base classes for Camera, LiDAR, and Radar with configurable parameters.
- 🌦 **Environmental Modeling**: Simulates real-world complexities such as fog, rain, occlusion, and sensor noise.
- 🔄 **Monte Carlo Engine**: This engine enables thousands of simulation runs to statistically validate sensor and system performance.
- 🛰 **Scenario Customization**: Flexible API for defining static and dynamic object layouts, sensor fusion strategies, and detection models.
- 📊 **Data Analysis Tools**: Built-in analytics and metrics generation (precision, recall, FOV coverage, etc.)
- 📈 **Visualization**: Custom plotting scripts for spatial coverage, detection probability, and sensor overlap.

---

## Repository Structure

IS597\_Final\_Project/
 - main.py                      # Entry point for running simulations
 - README.md                    # This file
 - config/
   - sensor\_configs.py        # Predefined sensor setup parameters
   - \*.png / \*.webp           # Visual assets for documentation
 - core/
   - position.py              # Vehicle and object positioning logic
   - sensor\_system.py         # Composite sensor management
 - examples/
   - custom\_scenarios.py      # Sample use-case simulations
 - sensors/
   - base.py                  # Sensor base class
   - camera.py                # Camera implementation
   - lidar.py                 # LiDAR implementation
   - radar.py                 # Radar implementation
 - simulation/
   - detection.py             # Object detection and validation logic
   - environment.py           # Weather and scene configuration
   - monte\_carlo.py           # Simulation runner and aggregator
 - utils/
   - analysis.py              # Evaluation metrics and data post-processing
 - visualization/
   - plots.py                 # Plotting and result visualization tools

---

## Getting Started

### 🛠 Requirements

- Python 3.8+
- matplotlib
- numpy
- pandas

> Install dependencies using:
pip install -r requirements.txt

### 🚀 Running a Simulation

Execute the main script to start a simulation:
python main.py


You can customize scenarios via 'examples/custom_scenarios.py' or modify sensor settings in 'config/sensor_configs.py'.

---

## Simulation Objectives

This framework is designed to answer key questions like:

* How do different sensor types perform under adverse weather?
* What is the statistical likelihood of object detection failure?
* Can sensor fusion reduce uncertainty in critical decision-making?
* What configuration yields the most robust perception pipeline?

---

## Visual Outputs

Plots include:

* Detection heatmaps
* False positive/negative rates
* Sensor range overlap diagrams
* Monte Carlo distribution summaries

All visualizations are generated via 'visualization/plots.py'.

---

## Use Cases

* **Academic Research**: Explore the impact of environment and sensor fidelity on detection accuracy.
* **Industry Prototyping**: Validate sensor configurations for L2-L4 autonomy platforms.
* **Simulation-Based Testing**: Perform risk-aware system validation at scale.

---

## Contributing

We welcome enhancements to sensors, fusion strategies, scenario modeling, and analytics. Fork the repo and submit a pull request for review.

---

## License

This project is intended for academic and non-commercial research use. For commercial applications or licensing inquiries, please contact the maintainers.

---

## Authors

Developed by Harishankar Kartha, Bharath Ganesh & Shantanu Roy as part of the IS597 Final Project (Spring 2025), University of Illinois Urbana-Champaign.

---

## Acknowledgements

* Tesla and Mercedes-Benz sensor suite diagrams (used for educational illustration)
* Inspiration from industry-grade simulators like CARLA and NVIDIA DriveSim
