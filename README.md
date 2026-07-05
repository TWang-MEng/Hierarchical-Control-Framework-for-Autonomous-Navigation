# Hierarchical Control Framework for Autonomous Navigation

[Status: Private Beta] | [Environment: CARLA 0.9.15] | [Language: Python 3.8+]

> Notice: This repository currently serves as a demonstration portfolio for academic and research evaluation. The source code is maintained privately during the active development phase and will be open-sourced upon the full completion and publication of the project.

## 1. Project Overview
This project introduces an advanced hierarchical control framework designed for highly interactive scenarios. The architecture strictly decouples high-level intent generation from low-level continuous kinematic execution. By introducing deterministic boundary constraints, it ensures safe and stable navigation for autonomous platforms across complex dynamic environments.

## 2. Video Demonstrations
The following videos demonstrate the simulation results of the current architecture in the CARLA environment.

https://github.com/user-attachments/assets/9d08c2e4-4122-4364-a0a9-60a8417a65b6

## 3. System Architecture Highlights
This framework formulates navigational behavior as a constraint-driven optimization problem, thereby avoiding the inherent fragility of traditional rule-based logic.

* Dual-Track Control Routing: A flexible operational architecture that seamlessly bridges intent-based tactical decision-making with micro-level trajectory tracking.
* Interaction-Aware Safety Envelope: Generates predictive boundaries based on dynamic flow heuristics, providing strict mathematical constraints for downstream planners.
* Frenet-Space Local Trajectory Planning: Combining topological structures with dynamic boundary conditions, the planner generates smooth, kinematically constrained candidate trajectories in real-time to accommodate complex maneuvers, such as dynamic obstacle avoidance and target following.
* High-Precision Closed-Loop Trajectory Tracking: Building upon classical lateral tracking algorithms, a specialized compensation mechanism is designed to address system actuation delays and rigid-body posture. This ensures precise trajectory adherence and platform stability during high-speed dynamic maneuvers.
* 3D Geometry-Based Continuous Clearance Resolution: In dense interactive environments, the system executes high-precision spatial clearance computations relying on the platform's exact 3D physical bounding box, establishing rigorous collision-avoidance boundaries for both the decision and execution layers.

## 4. Development Roadmap
The project is being developed in structured phases, systematically transitioning towards a fully generalized predictive optimal control framework.

- [x] Phase 1: Interactive Environment & Tactical Decision Layer
  - Implementation of the simulation infrastructure and the predictive safety envelope generation module for longitudinal dynamics.
- [x] Phase 2: Frenet-Space Optimal Planning (FOT)
  - Implementation of continuous target pseudo-waypoint generation and robust local trajectory optimization.
- [ ] Phase 3: Receding Horizon Model Predictive Control (MPC) Integration (Ongoing)
  - Transitioning the multi-variable optimization logic into a Model Predictive Control framework to handle complex state and action constraints over extended time horizons.
- [ ] Phase 4: Comprehensive Open Source Release
  - Complete codebase documentation, structural cleanup, and public repository launch.

## 5. Contact
For detailed inquiries regarding the theoretical formulations, optimization constraints, or further demonstration requests, please contact the author directly.
