# Awesome Autonomous Drone Racing [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated personal list of resources for autonomous drone racing competitions, including AI Grand Prix, A2RL, and AlphaPilot.

## Contents

- [Competitions](#competitions)
- [Simulators](#simulators)
- [Frameworks & Libraries](#frameworks--libraries)
- [State Estimation](#state-estimation)
- [Datasets](#datasets)
- [Papers](#papers)
- [Tutorials & Courses](#tutorials--courses)
- [Hardware](#hardware)
- [Community](#community)
- [AI Research](#ai-research)

## Competitions

### Active

- [AI Grand Prix](https://aigrandprix.com) - Anduril's $500K autonomous drone racing competition. Virtual qualification April-June 2026, finals November 2026 in Columbus, OH.


### Historical

- [A2RL](https://a2rl.io) - Abu Dhabi Autonomous Racing League. First competition where AI defeated human world champions (TU Delft, April 2025).
- [Purdue Autonomous Drone Racing](https://pylon-racing.geddes.rcac.purdue.edu/) - Indoor fixed-wing pylon racing with simulation-to-real format. Competition begins November 2025.
- [24th Roboracer Autonomous Grand Prix @ ICRA 2026](https://2026.ieee-icra.org/event/the-24th-roboracer-autonomous-grand-prix-competition/) - 1:10 scale autonomous racing using AutoDRIVE Ecosystem. 135+ participants at ICRA 2024, 89+ universities.
- [AlphaPilot](https://www.herox.com/alphapilot) - Lockheed Martin AI drone racing challenge (2019). $1M prize won by TU Delft MAVLab.
- [Game of Drones](https://microsoft.github.io/AirSim-NeurIPS2019-Drone-Racing/) - NeurIPS 2019 competition using Microsoft AirSim. Framework still available for benchmarking.
- [IROS Autonomous Drone Racing](https://www.uzh.ch/cmsssl/ifi/en/ailab/news/iros18-autonomous-drone-race.html) - IROS 2018 competition won by UZH-RPG.

## Simulators

### GPU-Parallel (Isaac-Based)

- [Aerial Gym Simulator](https://github.com/ntnu-arl/aerial_gym_simulator) - Isaac Gym with GPU-parallelized geometric controllers supporting 100,000+ parallel drones. ICRA 2024 paper.
- [Isaac Gym](https://developer.nvidia.com/isaac-gym) - NVIDIA's GPU-accelerated physics simulation for RL training.
- [OmniDrones](https://github.com/btx0424/OmniDrones) - Isaac Sim 4.1.0 achieving 10⁵ steps/second. 4 drone models, 5 sensor modalities, 15+ benchmark tasks. IEEE RA-L 2024.
- [Pegasus Simulator](https://github.com/PegasusSimulator/PegasusSimulator) - Isaac Sim extension with native PX4/ArduPilot and ROS2 support. Photorealistic environments.

### Traditional Physics Engines

- [Agilicious](https://github.com/uzh-rpg/agilicious) - Complete quadrotor hardware/software stack from UZH-RPG. Demonstrated 5g maneuvers at 70 km/h.
- [AirSim](https://github.com/microsoft/AirSim) - Microsoft's Unreal Engine-based simulator with drone racing environments.
- [AirSim Drone Racing Lab](https://github.com/microsoft/AirSim-Drone-Racing-Lab) - Competition framework built on AirSim for the NeurIPS Game of Drones.
- [Cosys-AirSim](https://github.com/Cosys-Lab/Cosys-AirSim) - Actively maintained AirSim fork updated for Unreal Engine 5.5 with GPU-LiDAR and new sensors.
- [CrazySim](https://github.com/gtfactslab/CrazySim) - First proper software-in-the-loop simulator for Crazyflie with Gazebo Sim/ROS2 integration. ICRA 2024.
- [Flightmare](https://github.com/uzh-rpg/flightmare) - UZH-RPG flexible simulator with Unity rendering, 200kHz physics, and OpenAI Gym API.
- [FlightForge](https://arxiv.org/abs/2502.05038) - UE5-based simulator with procedural environment generation for Sprin-D Autonomous Flight Challenge 2024.
- [gym_multirotor](https://github.com/adipandas/gym_multirotor) - MuJoCo-based quadrotor environments compatible with stable-baselines3.
- [gym-pybullet-drones](https://github.com/utiasDSL/gym-pybullet-drones) - Gymnasium-compatible RL environments with Crazyflie dynamics and ROS 2 support.
- [KestrelFPV](https://github.com/eleurent/KestrelFPV) - Unity3D FPV racing simulator with realistic aerodynamics and multiplayer support.
- [RotorS](https://github.com/ethz-asl/rotors_simulator) - ETH Zurich MAV simulation framework for Gazebo.

## Frameworks & Libraries

### Flight Control

- [ArduPilot](https://github.com/ArduPilot/ardupilot) - Open-source autopilot supporting multi-copters, planes, and rovers.
- [Betaflight](https://github.com/betaflight/betaflight) - Flight controller firmware popular in FPV racing, increasingly used for autonomous research.
- [Indiflight](https://github.com/tudelft/indiflight) - TU Delft research firmware with incremental nonlinear dynamic inversion control.
- [Paparazzi UAV](https://github.com/paparazzi/paparazzi) - Complete open-source autopilot system from TU Delft MAVLab.
- [PX4 Autopilot](https://github.com/PX4/PX4-Autopilot) - Professional open-source flight control stack with extensive documentation.

### Middleware & Communication

- [MAVSDK](https://github.com/mavlink/MAVSDK) - MAVLink SDK for Python, C++, and other languages.
- [MAVROS](https://github.com/mavlink/mavros) - ROS interface for MAVLink-based autopilots.
- [ROS 2](https://docs.ros.org/en/humble/) - Robot Operating System for building drone autonomy stacks.

### Control & Planning

- [acados](https://github.com/acados/acados) - Real-time nonlinear MPC solver with Python interface.
- [acmpc_public](https://github.com/uzh-rpg/acmpc_public) - Actor-Critic MPC combining RL performance with MPC robustness.
- [Control Toolbox](https://github.com/ethz-adrl/control-toolbox) - Production-grade C++ MPC with quadrotor model. iLQR, Gauss-Newton, IPOPT/SNOPT/HPIPM solvers. 1.6k stars.
- [Fast-Planner](https://github.com/HKUST-Aerial-Robotics/Fast-Planner) - Real-time UAV replanning using gradient-based B-spline optimization with ESDF collision avoidance. 2.5k+ stars.
- [mav_trajectory_generation](https://github.com/ethz-asl/mav_trajectory_generation) - Minimum-snap trajectory generation based on Mellinger & Kumar. Gold standard for aggressive flight. 800+ stars.
- [rpg_mpc](https://github.com/uzh-rpg/rpg_mpc) - Model Predictive Control for quadrotors from UZH-RPG.
- [rpg_time_optimal](https://github.com/uzh-rpg/rpg_time_optimal) - CPC trajectory planning for time-optimal quadrotor paths.
- [TinyMPC](https://github.com/TinyMPC/TinyMPC) - High-speed MPC on microcontrollers using ADMM. Best Paper Award in Automation at ICRA 2024.
- [TOPP-RA](https://github.com/hungpham2511/toppra) - Time-optimal path parameterization with 100% success rate in milliseconds.
- [uav_geometric_control](https://github.com/fdcl-gwu/uav_geometric_control) - Reference SE(3) tracking control in C++, MATLAB, and Python for extreme attitude maneuvers.

### Reinforcement Learning

- [CleanRL](https://github.com/vwxyzjn/cleanrl) - Single-file RL implementations including PPO, ideal for learning.
- [rl-tools](https://github.com/rl-tools/rl-tools) - Ultra-fast RL training (~4s for pendulum) with microcontroller deployment. Includes quadrotor examples.
- [skrl](https://github.com/Toni-SM/skrl) - Modular RL library supporting Isaac Gym for parallel training.
- [Stable-Baselines3](https://github.com/DLR-RM/stable-baselines3) - Reliable RL algorithm implementations in PyTorch.

### Racing Implementations

- [DeepPilot](https://github.com/QuetzalCpp/DeepPilot) - End-to-end CNN racing from camera images to flight commands using temporal mosaic. 25 FPS.
- [GateNet](https://github.com/open-airlab/GateNet) - Shallow CNN for gate detection at 60 Hz on Jetson TX2 with fish-eye support and AU-DR dataset.
- [Learning to Fly](https://github.com/arplaboratory/learning-to-fly) - Sim-to-real transfer for direct RPM control after only 18 seconds of training. NYU ARPL.
- [lsy_drone_racing](https://github.com/utiasDSL/lsy_drone_racing) - Complete educational framework with progressive difficulty and sim-to-real to Crazyflie. University course.

## State Estimation

- [LARVIO](https://github.com/PetWorm/LARVIO) - Lightweight, Accurate and Robust monocular VIO.
- [msckf_vio](https://github.com/KumarRobotics/msckf_vio) - Robust stereo VIO using Multi-State Constraint Kalman Filter.
- [OpenVINS](https://github.com/rpng/open_vins) - Winner of IROS 2019 FPV VIO Competition. Handles speeds up to 23.4 m/s with online calibration.
- [ORB-SLAM3](https://github.com/UZ-SLAMLab/ORB_SLAM3) - Visual-Inertial SLAM supporting monocular, stereo, and RGB-D cameras.
- [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion) - Multi-sensor fusion for robust state estimation.

## Datasets

- [AirSim Drone Racing Dataset](https://github.com/microsoft/AirSim-NeurIPS2019-Drone-Racing) - Synthetic data from NeurIPS 2019 Game of Drones with multiple environments and sensor modalities.
- [Blackbird Dataset](https://github.com/mit-fast/Blackbird-Dataset) - MIT aggressive flight dataset with ground truth from motion capture.
- [EuRoC MAV Dataset](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets) - ETH Zurich visual-inertial datasets for benchmarking.
- [MILUV](https://arxiv.org/abs/2401.00000) - Multi-UAV Indoor Localization: 217 minutes across 36 experiments with UWB, stereo vision, and motion-capture ground truth.
- [SimD3](https://arxiv.org/abs/2601.14742) - Synthetic dataset from Cosys-AirSim/UE5 with diverse environments and adverse weather conditions (January 2025).
- [TII-RATM Dataset](https://github.com/tii-racing/drone-racing-dataset) - 4000+ hours of multimodal racing data including autonomous and human-piloted flights (>21 m/s). RA-L 2024.
- [UZH-FPV Drone Racing Dataset](https://fpv.ifi.uzh.ch/) - High-speed racing data with event cameras, standard cameras, and IMU.
- [VAPAR](https://github.com/ntnu-arl/VAPAR) - Visual-Aware Planning for autonomous racing dataset.

## Papers

### Foundational

- [A Benchmark Comparison of Learned Control Policies for Agile Quadrotor Flight](https://arxiv.org/abs/2210.09485) - Systematic comparison of RL approaches for quadrotor control.
- [Beauty and the Beast: Optimal Methods Meet Learning for Drone Racing](https://arxiv.org/abs/1810.06224) - UZH-RPG's hybrid approach combining perception with optimal control.
- [Deep Drone Racing: From Simulation to Reality with Domain Randomization](https://arxiv.org/abs/1905.09727) - Key paper on sim-to-real transfer for drone racing.
- [Learning High-Speed Flight in the Wild](https://www.science.org/doi/10.1126/scirobotics.abg5810) - Science Robotics paper on agile flight through complex environments.

### Competition Winners

- [Champion-level drone racing using deep reinforcement learning](https://www.nature.com/articles/s41586-023-06419-4) - Nature 2023. UZH's Swift system beating human champions.
- [Guidance & Control Networks for Time-Optimal Quadrotor Flight](https://arxiv.org/abs/2305.14324) - TU Delft's winning A2RL approach with direct motor control at 500Hz.
- [The Winning Solution to the 2019 AlphaPilot Challenge](https://www.research-collection.ethz.ch/handle/20.500.11850/469934) - Technical report from MAVLab's $1M win.

### Sim-to-Real & Learning

- [Learning Generalizable Policy for Obstacle-Aware Autonomous Drone Racing](https://arxiv.org/abs/2411.04246) - Deep RL with domain randomization achieving 70 km/h in cluttered environments.
- [Learning to Fly in Seconds](https://arxiv.org/abs/2311.13081) - Sim-to-real transfer after only 18 seconds of training. Asymmetric actor-critic with curriculum learning. RA-L 2024.
- [Time-Optimal Planning for Long-Range Quadrotor Flights](https://arxiv.org/abs/2407.17944) - Polynomial-based optimal synthesis validated at 8.86 m/s peak velocity.
- [Unlocking Aerobatic Potential of Quadcopters](https://www.science.org/journal/scirobotics) - Science Robotics April 2025. First system achieving professional-pilot-level aerobatics autonomously.

### Perception

- [Fast and Accurate Gate Detection for Autonomous Drone Racing](https://arxiv.org/abs/2012.04512) - U-Net based corner detection achieving 10.5ms inference.
- [MonoRace: Visual Odometry for Racing Drones](https://ieeexplore.ieee.org/document/9561785) - Monocular VIO optimized for racing conditions.

### Control

- [MPCC++: Model Predictive Contouring Control for Time-Optimal Racing](https://arxiv.org/abs/2402.03456) - MPC approach with 100% success rate in real-world racing.
- [NeuroBEM: Hybrid Neural Network/Blade Element Momentum](https://arxiv.org/abs/2302.02988) - 50% improved dynamics prediction for aggressive flight.
- [TinyMPC: Model-Predictive Control on Resource-Constrained Microcontrollers](https://arxiv.org/abs/2310.16985) - Best Paper in Automation ICRA 2024. Real-time MPC on Crazyflie.

## Tutorials & Courses

### University Courses

- [Aerial Robotics (Penn, Coursera)](https://www.coursera.org/learn/robotics-flight) - Fundamentals of quadrotor dynamics and control.
- [MIT Visual Navigation for Autonomous Vehicles](https://vnav.mit.edu/) - State-of-the-art visual navigation and SLAM by Luca Carlone.
- [University of Maryland ENAE788M](http://prg.cs.umd.edu/enae788m) - Complete videos, slides, and ROS-based assignments. Most comprehensive free aerial robotics course.

### Professional Training

- [IEEE RAS Summer School on Multi-robot Systems](https://mrs.fel.cvut.cz/summer-school-2026/) - Hands-on aerial robotics at CTU Prague. 2026 edition accepting applications.
- [Udacity Flying Car Nanodegree](https://www.udacity.com/course/flying-car-nanodegree--nd787) - Planning, controls, and estimation with real drone labs. 4 months.

### Self-Study

- [awesome-dronecraft](https://github.com/ntakouris/awesome-dronecraft) - Learning roadmap from programmer to drone engineer.
- [awesome-RL-for-UAVs](https://github.com/GongXudong/awesome-RL-for-UAVs) - Curated RL papers and code for UAV control including racing and sim-to-real.
- [Intelligent Quads (YouTube)](https://www.youtube.com/@IntelligentQuads) - Beginner-to-advanced coverage of Ardupilot, MAVlink, ROS, and Gazebo.
- [MIT Beaver Works UAV Racing](https://beaverworks.ll.mit.edu/CMS/bw/bwsi_uav) - Four-week summer program with public course materials.
- [PX4 Developer Guide](https://docs.px4.io/main/en/development/development.html) - Official documentation for PX4 development.
- [ROS 2 Tutorials](https://docs.ros.org/en/humble/Tutorials.html) - Official ROS 2 learning path.

## Hardware

### Compute Platforms

- [Khadas VIM4](https://www.khadas.com/vim4) - ARM-based SBC with NPU for edge inference.
- [NVIDIA Jetson Orin NX](https://developer.nvidia.com/embedded/jetson-orin) - 100 TOPS AI performance. De facto standard for championship racing (A2RL). YOLOv8-Pose at 62 Hz.
- [NVIDIA Jetson Xavier NX](https://developer.nvidia.com/embedded/jetson-xavier-nx) - Previous generation, common in research platforms.

### Flight Controllers

- [Foxeer H7](https://www.foxeer.com/) - Used in A2RL/TII racing specification with Betaflight 4.4.0.
- [Holybro Pixhawk 6X](https://holybro.com/products/pixhawk-6x) - Latest Pixhawk standard with dual IMUs.
- [mRobotics Control Zero H7](https://store.mrobotics.io/product-p/mro-control-zero-h7.htm) - Compact PX4-compatible flight controller.
- [SpeedyBee F405 V4](https://www.speedybee.com/speedybee-f405-v4-bls-55a-30x30-fc-esc-stack/) - Popular Betaflight/ArduPilot compatible FC.

### Cameras

- [iniVation mDAVIS 346](https://inivation.com/buy/) - Event camera with 130% VIO accuracy improvement over standard frames at high speeds.
- [Intel RealSense D435i](https://www.intelrealsense.com/depth-camera-d435i/) - Depth + IMU for indoor navigation.
- [Leopard Imaging IMX264](https://www.leopardimaging.com/product/autonomous-camera/maxim-gmsl-cameras/) - Global shutter camera used in AlphaPilot.
- [Prophesee Event Cameras](https://www.prophesee.ai/) - Event-based sensing for high-speed motion.

### Reference Platforms

- [A2RL/TII Open Design](https://github.com/tii-racing) - ~966g carbon fiber frame achieving 100+ km/h with 4:1 thrust ratio.
- [Bitcraze Crazyflie 2.1+](https://www.bitcraze.io/products/crazyflie-2-1/) - Nano quadrotor with AI-deck and Lighthouse positioning. Standard for indoor RL research.
- [Bitcraze Crazyflie Brushless](https://www.bitcraze.io/) - 41g brushless variant with 7-10 min flight time.
- [Holybro X500 V2](https://holybro.com/products/x500-v2-kit) - PX4 development platform.
- [ModalAI Starling](https://www.modalai.com/products/starling) - Ready-to-fly autonomous drone with VOXL compute.

## Community

### Discord & Chat

- [Drone Community Discord](https://discord.gg/drones) - Large general drone community with FPV and autonomous channels.
- [Open Robotics Discord](https://discord.gg/openrobotics) - Official ROS and Gazebo community.
- [Reinforcement Learning Discord](https://discord.gg/xhfNqQv) - RL research discussions including robotics applications.

### Forums & Q&A

- [PX4 Discuss](https://discuss.px4.io/) - Official PX4 community forum.
- [Robotics Stack Exchange](https://robotics.stackexchange.com/) - Q&A for robotics including drones.
- [ROS Discourse](https://discourse.ros.org/) - Official ROS community forum.

### Subreddits

- [r/drones](https://www.reddit.com/r/drones/) - General drone community.
- [r/fpv](https://www.reddit.com/r/fpv/) - FPV racing and freestyle community.
- [r/reinforcementlearning](https://www.reddit.com/r/reinforcementlearning/) - RL research and applications.
- [r/robotics](https://www.reddit.com/r/robotics/) - Robotics projects and research.
- [r/ROS](https://www.reddit.com/r/ROS/) - Robot Operating System community.

### Research Labs

- [ETH Zurich Autonomous Systems Lab](https://asl.ethz.ch/) - RotorS, MAV research.
- [HKUST Aerial Robotics Group](https://uav.hkust.edu.hk/) - Fast-Planner, VINS-Fusion.
- [MIT FAST Lab](https://groups.csail.mit.edu/rrg/) - Aggressive flight and Blackbird dataset.
- [NTNU Autonomous Robots Lab](https://www.autonomousrobotslab.com/) - Aerial Gym, VAPAR dataset.
- [NYU Agile Robotics and Perception Lab](https://wp.nyu.edu/arpl/) - Learning to Fly in Seconds.
- [TU Delft MAVLab](https://mavlab.tudelft.nl/) - A2RL and AlphaPilot champions, Paparazzi UAV, G&CNets.
- [UZH Robotics and Perception Group](https://rpg.ifi.uzh.ch/) - Flightmare, Agilicious, Swift. The leading academic lab in drone racing.
- [UTIAS Dynamic Systems Lab](http://dsl.utias.utoronto.ca/) - gym-pybullet-drones, lsy_drone_racing, Crazyflie research.

## AI Research

> **Note:** The following resources were generated by AI and may contain inaccuracies. See disclaimers within each document.

- [Winning at Autonomous Drone Racing](ai-research/winning-autonomous-drone-racing.md) - Technical analysis of competition-winning approaches including G&CNets, PPO training, and sim-to-real transfer strategies.

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
