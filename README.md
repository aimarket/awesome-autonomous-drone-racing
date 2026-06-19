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
- [Experimental & Emerging](#experimental--emerging)

## Competitions

### Active

- [AI Grand Prix](https://theaigrandprix.com) - $500K autonomous drone race conceived by Anduril's Palmer Luckey, run with the Drone Champions League on identical Neros Technologies drones (software only, no human pilots). Inaugural 2026 season: virtual qualifiers (May–July), a Southern California physical qualifier (September), and finals in Ohio (November).
- [A2RL](https://a2rl.io) - Abu Dhabi Autonomous Racing League. Vision-only autonomous racing (single forward-facing RGB camera + IMU; LiDAR/stereo/GPS prohibited). In April 2025 it became the first event where AI beat human champions (won by TU Delft); at the Jan 2026 Drone Championship (UMEX), FPV world champion Minchan Kim beat the autonomous drone in a best-of-nine, while TII Racing set the fastest AI lap (12.032s) and MAVLab won the multi-drone race.


### Historical
- [Purdue Autonomous Drone Racing](https://pylon-racing.geddes.rcac.purdue.edu/) - Indoor fixed-wing pylon racing with simulation-to-real format. Competition held December 2025.
- [27th Roboracer Autonomous Grand Prix @ ICRA 2026](https://icra2026-race.roboracer.ai/) - 1:10 scale autonomous racing, held at ICRA 2026 (VIECON, Vienna, June 1–5 2026).
- [AlphaPilot](https://www.herox.com/alphapilot) - Lockheed Martin AI drone racing challenge (2019). Over $2M in prizes, won by TU Delft MAVLab.
- [Game of Drones](https://microsoft.github.io/AirSim-NeurIPS2019-Drone-Racing/) - NeurIPS 2019 competition using Microsoft AirSim. Framework still available for benchmarking.
- [IROS Autonomous Drone Racing](https://www.ifi.uzh.ch/en/rpg/news/RPG-won-the-IROS-2018-Autonomous-Drone-Race.html) - IROS 2018 competition won by UZH-RPG.

## Simulators

### GPU-Parallel (Isaac-Based)

- [Aerial Gym Simulator](https://github.com/ntnu-arl/aerial_gym_simulator) - Isaac Gym with GPU-parallelized geometric controllers supporting 100,000+ parallel drones. IEEE RA-L 2025.
- [Isaac Gym](https://developer.nvidia.com/isaac-gym) - NVIDIA's GPU-accelerated physics simulation for RL training. Now legacy; superseded by Isaac Lab (built on Isaac Sim).
- [OmniDrones](https://github.com/btx0424/OmniDrones) - Isaac Sim 4.1.0 with multi-rotor RL environments. IEEE RA-L 2024. No longer actively maintained.
- [Pegasus Simulator](https://github.com/PegasusSimulator/PegasusSimulator) - Isaac Sim extension with native PX4/ArduPilot and ROS2 support. Photorealistic environments.

### Traditional Physics Engines

- [Agilicious](https://github.com/uzh-rpg/agilicious) - Complete quadrotor hardware/software stack from UZH-RPG. Demonstrated 5g maneuvers at 70 km/h.
- [AirSim](https://github.com/microsoft/AirSim) - Microsoft's Unreal Engine-based simulator with drone racing environments. Development frozen; succeeded by the commercial Project AirSim.
- [AirSim Drone Racing Lab](https://github.com/microsoft/AirSim-Drone-Racing-Lab) - Competition framework built on AirSim for the NeurIPS Game of Drones. Archived (read-only) since June 2026.
- [Cosys-AirSim](https://github.com/Cosys-Lab/Cosys-AirSim) - AirSim fork updated for Unreal Engine 5.5 with GPU-LiDAR and new sensors. No longer actively maintained.
- [CrazySim](https://github.com/gtfactslab/CrazySim) - First proper software-in-the-loop simulator for Crazyflie with Gazebo Sim/ROS2 integration. ICRA 2024.
- [Flightmare](https://github.com/uzh-rpg/flightmare) - UZH-RPG flexible simulator with Unity rendering, 200kHz physics, and OpenAI Gym API.
- [FlightForge](https://arxiv.org/abs/2502.05038) - UE5-based simulator with procedural environment generation for Sprin-D Autonomous Flight Challenge 2024.
- [gym_multirotor](https://github.com/adipandas/gym_multirotor) - MuJoCo-based quadrotor environments compatible with stable-baselines3.
- [gym-pybullet-drones](https://github.com/learnsyslab/gym-pybullet-drones) - Gymnasium-compatible RL environments with Crazyflie dynamics.
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
- [Control Toolbox](https://github.com/ethz-adrl/control-toolbox) - Production-grade C++ MPC with quadrotor model. iLQR, Gauss-Newton, IPOPT/SNOPT/HPIPM solvers. 1.7k stars.
- [Fast-Planner](https://github.com/HKUST-Aerial-Robotics/Fast-Planner) - Real-time UAV replanning using gradient-based B-spline optimization with ESDF collision avoidance. 3.2k+ stars.
- [mav_trajectory_generation](https://github.com/ethz-asl/mav_trajectory_generation) - Minimum-snap trajectory generation based on Mellinger & Kumar. Gold standard for aggressive flight.
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
- [lsy_drone_racing](https://github.com/learnsyslab/lsy_drone_racing) - Complete educational framework with progressive difficulty and sim-to-real to Crazyflie. University course.

## State Estimation

- [LARVIO](https://github.com/PetWorm/LARVIO) - Lightweight, Accurate and Robust monocular VIO.
- [msckf_vio](https://github.com/KumarRobotics/msckf_vio) - Robust stereo VIO using Multi-State Constraint Kalman Filter.
- [OpenVINS](https://github.com/rpng/open_vins) - Winner of the IROS 2019 FPV VIO Competition on the UZH-FPV racing dataset (ground-truth speeds up to 23.4 m/s). Supports online calibration.
- [ORB-SLAM3](https://github.com/UZ-SLAMLab/ORB_SLAM3) - Visual-Inertial SLAM supporting monocular, stereo, and RGB-D cameras.
- [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion) - Multi-sensor fusion for robust state estimation.

## Datasets

- [AirSim Drone Racing Dataset](https://github.com/microsoft/AirSim-NeurIPS2019-Drone-Racing) - Synthetic data from NeurIPS 2019 Game of Drones with multiple environments and sensor modalities. Archived (read-only) since June 2026.
- [Blackbird Dataset](https://github.com/mit-aera/Blackbird-Dataset) - MIT aggressive flight dataset with ground truth from motion capture.
- [EuRoC MAV Dataset](https://projects.asl.ethz.ch/datasets/doku.php?id=kmavvisualinertialdatasets) - ETH Zurich visual-inertial datasets for benchmarking.
- [MILUV](https://arxiv.org/abs/2504.14376) - Multi-UAV indoor localization dataset: 217 minutes across 36 experiments with UWB, stereo vision, and motion-capture ground truth (indoor localization, not high-speed racing).
- [TII-RATM Dataset](https://github.com/tii-racing/drone-racing-dataset) - Multimodal racing data including autonomous and human-piloted flights (>21 m/s). RA-L 2024.
- [UZH-FPV Drone Racing Dataset](https://fpv.ifi.uzh.ch/) - High-speed racing data with event cameras, standard cameras, and IMU.
- [VAPAR](https://github.com/uzh-rpg/VAPAR) - UZH-RPG dataset of flight trajectories, RGB, and human eye-gaze for visual-attention-aware drone racing (Pfeiffer et al., PLOS ONE 2022).

## Papers

### Foundational

- [A Benchmark Comparison of Learned Control Policies for Agile Quadrotor Flight](https://arxiv.org/abs/2202.10796) - Systematic comparison of learned control policies for agile quadrotor flight. ICRA 2022.
- [Beauty and the Beast: Optimal Methods Meet Learning for Drone Racing](https://arxiv.org/abs/1810.06224) - UZH-RPG's hybrid approach combining perception with optimal control.
- [Deep Drone Racing: From Simulation to Reality with Domain Randomization](https://arxiv.org/abs/1905.09727) - Key paper on sim-to-real transfer for drone racing.
- [Learning High-Speed Flight in the Wild](https://www.science.org/doi/10.1126/scirobotics.abg5810) - Science Robotics paper on agile flight through complex environments.

### Competition Winners

- [Champion-level drone racing using deep reinforcement learning](https://www.nature.com/articles/s41586-023-06419-4) - Nature 2023. UZH's Swift system beating human champions.
- [Guidance & Control Networks for Time-Optimal Quadcopter Flight](https://arxiv.org/abs/2305.02705) - TU Delft MAVLab's neural-network approximation of time-optimal control (G&CNets) for aggressive quadrotor flight.
- [AlphaPilot: Autonomous Drone Racing](https://arxiv.org/abs/2005.12813) - UZH-RPG's vision-based full-stack racing system for the 2019 Lockheed Martin AlphaPilot Challenge (Foehn et al.).

### Sim-to-Real & Learning

- [Learning Generalizable Policy for Obstacle-Aware Autonomous Drone Racing](https://arxiv.org/abs/2411.04246) - Deep RL with domain randomization achieving 70 km/h in cluttered environments.
- [Learning to Fly in Seconds](https://arxiv.org/abs/2311.13081) - Sim-to-real transfer after only 18 seconds of training. Asymmetric actor-critic with curriculum learning. RA-L 2024.
- [Time-Optimal Planning for Long-Range Quadrotor Flights](https://arxiv.org/abs/2407.17944) - Polynomial-based optimal synthesis validated at 8.86 m/s peak velocity.
- [Unlocking Aerobatic Potential of Quadcopters](https://www.science.org/doi/10.1126/scirobotics.adp9905) - Science Robotics (ZJU FAST Lab, 2025). Autonomous generation and execution of professional-level freestyle aerobatics.

### Perception

- [Continual Learning for Robust Gate Detection under Dynamic Lighting in Autonomous Drone Racing](https://arxiv.org/abs/2405.01054) - Continual-learning gate detector robust to changing illumination for onboard racing perception.
- [MonoRace: Winning Champion-Level Drone Racing with Robust Monocular AI](https://arxiv.org/abs/2601.15222) - TU Delft MAVLab onboard system using neural gate segmentation and a learned drone model for robust state estimation from a single rolling-shutter camera and IMU; won the 2025 A2RL Autonomous Drone Race.

### Control

- [MPCC++: Model Predictive Contouring Control for Time-Optimal Flight with Safety Constraints](https://arxiv.org/abs/2403.17551) - UZH-RPG MPC adding track/terminal safety constraints and residual aerodynamics for crash-free flight at 80+ km/h.
- [NeuroBEM: Hybrid Aerodynamic Quadrotor Model](https://arxiv.org/abs/2106.08015) - Hybrid neural-network/blade-element-momentum model with ~50% lower dynamics-prediction error for aggressive flight. RSS 2021.
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
- [NVIDIA Jetson Orin NX](https://developer.nvidia.com/embedded/jetson-orin) - Up to 157 TOPS AI performance. De facto standard for championship racing (A2RL). YOLOv8-Pose at 62 Hz.
- [NVIDIA Jetson Xavier NX](https://developer.nvidia.com/embedded/jetson-xavier-nx) - Previous generation, common in research platforms.

### Flight Controllers

- [Foxeer H7](https://www.foxeer.com/) - Used in A2RL/TII racing specification with Betaflight 4.4.0.
- [Holybro Pixhawk 6X](https://holybro.com/products/pixhawk-6x) - Latest Pixhawk standard with dual IMUs.
- [mRobotics Control Zero H7](https://store.mrobotics.io/product-p/mro-control-zero-h7.htm) - Compact PX4-compatible flight controller.
- [SpeedyBee F405 V4](https://www.speedybee.com/speedybee-f405-v4-bls-55a-30x30-fc-esc-stack/) - Popular Betaflight/ArduPilot compatible FC.

### Cameras

- [iniVation mDAVIS 346](https://inivation.com/buy/) - Event camera with 130% VIO accuracy improvement over standard frames at high speeds.
- [Intel RealSense D435i](https://www.realsenseai.com/products/depth-camera-d435i/) - Depth + IMU for indoor navigation. (RealSense is now an independent company at realsenseai.com.)
- [Leopard Imaging IMX264](https://leopardimaging.com/product-tag/imx264/) - Global shutter camera used in AlphaPilot.
- [Prophesee Event Cameras](https://www.prophesee.ai/) - Event-based sensing for high-speed motion.

### Reference Platforms

- [A2RL/TII Open Design](https://github.com/tii-racing) - ~966g carbon fiber frame achieving 100+ km/h with 4:1 thrust ratio.
- [Bitcraze Crazyflie 2.1+](https://www.bitcraze.io/products/crazyflie-2-1/) - Nano quadrotor with AI-deck and Lighthouse positioning. Standard for indoor RL research.
- [Bitcraze Crazyflie Brushless](https://www.bitcraze.io/) - 41g brushless variant with 7-10 min flight time.
- [Holybro X500 V2](https://holybro.com/products/px4-development-kit-x500-v2) - PX4 development platform.
- [Langostino](https://github.com/swarm-subnet/Langostino) - Complete open-source autonomous drone platform with hardware BOM, ROS2 stack, and RL-based autopilot using gym-pybullet-drones. Raspberry Pi companion computer with LiDAR and GPS.
- [ModalAI Starling 2 Max](https://www.modalai.com/products/starling-2-max) - Ready-to-fly autonomous drone with VOXL compute.

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
- [MIT Karaman Group](https://karaman.mit.edu/) - Aggressive/agile flight and the Blackbird dataset (Sertac Karaman, MIT LIDS).
- [NTNU Autonomous Robots Lab](https://www.autonomousrobotslab.com/) - Aerial Gym, VAPAR dataset.
- [NYU Agile Robotics and Perception Lab](https://wp.nyu.edu/arpl/) - Learning to Fly in Seconds.
- [TU Delft MAVLab](https://mavlab.tudelft.nl/) - A2RL and AlphaPilot champions, Paparazzi UAV, G&CNets.
- [UZH Robotics and Perception Group](https://rpg.ifi.uzh.ch/) - Flightmare, Agilicious, Swift. The leading academic lab in drone racing.
- [UTIAS Dynamic Systems Lab](https://www.dynsyslab.org/) - gym-pybullet-drones and Crazyflie research.

## AI Research

> **Note:** The following resources were generated by AI and may contain inaccuracies. See disclaimers within each document.

- [Winning at Autonomous Drone Racing](ai-research/winning-autonomous-drone-racing.md) - Technical analysis of competition-winning approaches including G&CNets, PPO training, and sim-to-real transfer strategies.

## Experimental & Emerging

- [Biological & Wetware Computing](experimental-computing/README.md) - Organoid intelligence, cultured neurons, and brain-computer interfaces for drone control.

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
