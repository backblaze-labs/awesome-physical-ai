# Awesome Physical AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

A curated list of open-source tools for physical AI and robotics — foundation models, world models, simulators, learning frameworks, benchmarks, and runtime.

Maintained by [Backblaze](https://www.backblaze.com).

### Related Lists

- [Awesome ML Data Pipelines](https://github.com/backblaze-labs/awesome-ml-data-pipelines)
- [Awesome Multimodal Data](https://github.com/backblaze-labs/awesome-multimodal-data)
- [Awesome Agent Infrastructure](https://github.com/backblaze-labs/awesome-agent-infrastructure)
- [Awesome Image Generation](https://github.com/backblaze-labs/awesome-image-generation)
- [Awesome Video Generation](https://github.com/backblaze-labs/awesome-video-generation)
- [Awesome Audio Generation](https://github.com/backblaze-labs/awesome-audio-generation)

## Contents

- [Robotics Foundation Models](#robotics-foundation-models)
- [World Models](#world-models)
- [Simulation and Physics Engines](#simulation-and-physics-engines)
- [Robot Learning Frameworks](#robot-learning-frameworks)
- [Datasets and Benchmarks](#datasets-and-benchmarks)
- [Robot Middleware and Runtime](#robot-middleware-and-runtime)
- [Teleop and Data Collection](#teleop-and-data-collection)
- [SDKs and Developer Tooling](#sdks-and-developer-tooling)
- [Templates and Example Projects](#templates-and-example-projects)

---

## Robotics Foundation Models

> Vision-language-action (VLA) and embodied foundation models you can fine-tune and deploy.

- **[OpenVLA](https://openvla.github.io)** – 7B-parameter open vision-language-action model trained on 970k demonstrations from Open X-Embodiment. Strong generalist manipulation baseline. [Docs](https://github.com/openvla/openvla)
- **[Octo](https://octo-models.github.io)** – Transformer-based generalist robot policy pretrained on 800k trajectories. Flexible conditioning on goal images or language. [Docs](https://github.com/octo-models/octo)
- **[CrossFormer](https://crossformer-model.github.io)** – Transformer policy trained on 900k trajectories across 30 embodiments. Single model weights control arms, wheeled robots, quadcopters, and quadrupeds via language or goal-image conditioning. [Docs](https://github.com/rail-berkeley/crossformer)
- **[HuggingFace SmolVLA](https://huggingface.co/blog/smolvla)** – Compact VLA model from HuggingFace designed to run on consumer hardware while retaining generalist behaviour. [Docs](https://github.com/huggingface/lerobot)
- **[openpi](https://github.com/Physical-Intelligence/openpi)** – Open-source code and weights for π0, π0-FAST, and π0.5 VLA models from Physical Intelligence. Fine-tuning recipes for ALOHA, DROID, and custom platforms. [Docs](https://www.pi.website/blog/openpi)
- **[Physical Intelligence π-0](https://www.physicalintelligence.company)** – General-purpose robot foundation model from Physical Intelligence. Weights partially released; commercial access via partners.
- **[RT-X / RT-2](https://robotics-transformer-x.github.io)** – Google DeepMind's RT-X family of generalist robotics transformers and the Open X-Embodiment dataset that underpins them.

## World Models

> Generative world models for physical simulation, planning, and synthetic data.

- **[V-JEPA 2](https://ai.meta.com/research/v-jepa/)** – Meta FAIR's non-generative video predictive model. Learns world representations useful for planning and robot perception. [Docs](https://github.com/facebookresearch/jepa)
- **[NVIDIA Cosmos](https://www.nvidia.com/en-us/ai/cosmos/)** – World foundation-model platform for physical AI. Cosmos-Predict generates physics-aware video from text, image, video, or sensor inputs. [Docs](https://docs.nvidia.com/cosmos/latest/introduction.html)
- **[1X World Model](https://www.1x.tech/discover/introducing-our-world-model)** – Humanoid-centric world model from 1X. Generates high-fidelity first-person rollouts for policy evaluation in simulation.

## Simulation and Physics Engines

> Physics simulators and training environments for robotics and embodied AI.

- **[Genesis](https://genesis-embodied-ai.github.io)** – Pure-Python physics platform for generalist embodied AI. Unifies rigid, soft, fluid, and differentiable simulation. [Docs](https://genesis-world.readthedocs.io) | SDK: Python (pip install genesis-world)
- **[PyBullet](https://pybullet.org)** – Python bindings for the Bullet physics engine. Still widely used for manipulation and locomotion baselines. [Docs](https://docs.google.com/document/d/10sXEhzFRSnvFcl3XxNGhnD4N2SedqwdAvK3dsihxVUA) | SDK: Python (pip install pybullet)
- **[MuJoCo](https://mujoco.org)** – DeepMind's fast multi-joint dynamics engine. Standard for contact-rich manipulation and locomotion research. [Docs](https://mujoco.readthedocs.io) | SDK: Python (pip install mujoco), C
- **[NVIDIA Isaac Lab](https://isaac-sim.github.io/IsaacLab/)** – Unified robot-learning framework on Isaac Sim. GPU-accelerated training with rich sensor and contact simulation. [Docs](https://isaac-sim.github.io/IsaacLab/source/setup/installation/index.html)
- **[Drake](https://drake.mit.edu)** – MIT/TRI's model-based design toolbox. Rigid-body dynamics, trajectory optimization, and system modeling for robotics. [Docs](https://drake.mit.edu/doxygen_cxx/index.html)
- **[Brax](https://github.com/google/brax)** – Google's differentiable physics engine in JAX. Massively parallel RL on a single accelerator. SDK: Python (pip install brax)
- **[Gazebo](https://gazebosim.org)** – Open-source robotics simulator with tight ROS 2 integration. Modern Gazebo (Harmonic/Ionic) is the successor to Gazebo Classic. [Docs](https://gazebosim.org/docs)
- **[Genie Sim](https://github.com/AgibotTech/genie_sim)** – Humanoid-focused simulation platform built on Isaac Sim. LLM-driven scene generation, 5,100+ validated assets, 200+ benchmark tasks, and zero-shot sim-to-real transfer toolchain. [Docs](https://agibot-world.com)
- **[Newton](https://github.com/newton-physics/newton)** – GPU-accelerated physics simulation engine built on NVIDIA Warp, co-developed by NVIDIA, Google DeepMind, and Disney Research. Integrates MuJoCo Warp as its primary backend. [Docs](https://developer.nvidia.com/newton-physics) | SDK: Python (pip install newton)
- **[robosuite](https://robosuite.ai)** – MuJoCo-based simulation framework and benchmark suite for robot learning. Supports humanoids, custom robot composition, and photorealistic rendering. [Docs](https://robosuite.ai/docs/overview.html) | SDK: Python (pip install robosuite)

## Robot Learning Frameworks

> Imitation learning, RL, and policy training toolkits targeting robot control.

- **[HuggingFace LeRobot](https://github.com/huggingface/lerobot)** – End-to-end robot-learning library from HuggingFace. Datasets on the Hub, policies, and low-cost reference hardware (SO-100). [Docs](https://huggingface.co/docs/lerobot) | SDK: Python (pip install lerobot)
- **[Stable-Baselines3](https://stable-baselines3.readthedocs.io)** – Reliable PyTorch implementations of popular RL algorithms. De-facto baseline for reproducible RL research. [Docs](https://stable-baselines3.readthedocs.io/en/master/) | SDK: Python (pip install stable-baselines3)
- **[Robomimic](https://robomimic.github.io)** – Research framework for imitation learning from human demonstrations. Standardized dataset format and algorithm zoo. [Docs](https://robomimic.github.io/docs/introduction/overview.html)
- **[MuJoCo Playground](https://playground.mujoco.org)** – GPU-accelerated suite of robot learning environments built on MJX. Supports locomotion, manipulation, and dexterous hands with zero-shot sim-to-real transfer. [Docs](https://github.com/google-deepmind/mujoco_playground) | SDK: Python (pip install playground)
- **[RLlib (Ray)](https://docs.ray.io/en/latest/rllib/index.html)** – Scalable RL library part of Ray. Distributes training across clusters; supports most standard algorithms. SDK: Python (pip install ray[rllib])

## Datasets and Benchmarks

> Public robot datasets, embodied AI benchmarks, and evaluation suites.

- **[ManiSkill](https://www.maniskill.ai)** – GPU-parallel manipulation benchmark built on SAPIEN. Millions of env-steps per second on a single GPU. [Docs](https://maniskill.readthedocs.io)
- **[Meta-World](https://meta-world.github.io)** – 50-task manipulation benchmark for meta-learning and multitask RL. [Docs](https://github.com/Farama-Foundation/Metaworld)
- **[RLBench](https://sites.google.com/view/rlbench)** – Large-scale benchmark for robot learning with 100+ tasks built on CoppeliaSim. [Docs](https://github.com/stepjam/RLBench)
- **[LIBERO](https://libero-project.github.io)** – Benchmark for lifelong robot learning. 130 tasks across four skill categories, with standard splits and evaluation protocols. [Docs](https://github.com/Lifelong-Robot-Learning/LIBERO)
- **[AgiBot World](https://agibot-world.com)** – Large-scale bimanual manipulation dataset with 1M+ trajectories from 100 robots across 100+ real-world scenarios. Includes the GO-1 foundation model and LeRobot-based toolchain. [Docs](https://github.com/OpenDriveLab/AgiBot-World)
- **[DROID](https://droid-dataset.github.io)** – 76k in-the-wild Franka manipulation trajectories (350 h) collected across 564 scenes at 13 institutions. Dataset, policy-learning code, and hardware setup guide are open source. [Docs](https://github.com/droid-dataset/droid_policy_learning)
- **[Open X-Embodiment](https://github.com/google-deepmind/open_x_embodiment)** – Collaborative dataset of 22 embodiments, 1M+ episodes, 527 skills. Standard training corpus for generalist policies. [Docs](https://robotics-transformer-x.github.io)
- **[RoboCasa](https://robocasa.ai)** – Large-scale simulation framework for household robot training. RoboCasa365 ships 365 tasks, 2,500+ kitchen scenes, and 2,200+ hours of demonstration data. [Docs](https://github.com/robocasa/robocasa)

## Robot Middleware and Runtime

> Messaging, scheduling, and dataflow layers for running robots in the real world.

- **[ROS 2](https://www.ros.org)** – Standard robotics middleware. DDS-based messaging, real-time support, and a massive ecosystem of drivers and tools. [Docs](https://docs.ros.org/en/jazzy/)
- **[Dora-rs](https://dora-rs.ai)** – Low-latency dataflow robotics runtime written in Rust. Python-friendly; often faster than ROS 2 for perception pipelines. [Docs](https://dora-rs.ai/docs/) | SDK: Python (pip install dora-rs), Rust

## Teleop and Data Collection

> Hardware kits and software for collecting demonstration data on real and simulated robots.

- **[LeRobot SO-100 Arm](https://github.com/TheRobotStudio/SO-ARM100)** – Open-source 6-DOF arm co-developed with HuggingFace LeRobot. ~$120 BOM; standard entry-point for homegrown robot data.
- **[Mobile ALOHA](https://mobile-aloha.github.io)** – Low-cost bimanual mobile-manipulation platform with open hardware and teleop code. Reference data-collection rig. [Docs](https://github.com/MarkFzp/mobile-aloha)
- **[GELLO](https://wuphilipp.github.io/gello_site/)** – Low-cost, 3D-printable intuitive teleoperation system for arm manipulators. Popular for collecting demonstration data. [Docs](https://github.com/wuphilipp/gello_software)

## SDKs and Developer Tooling

> Libraries for 3D, kinematics, manipulation, and general robotics development.

- **[Open3D](https://www.open3d.org)** – 3D data processing library with point-cloud registration, reconstruction, and a modern ML module. [Docs](https://www.open3d.org/docs/release/) | SDK: Python (pip install open3d), C++
- **[PyTorch3D](https://pytorch3d.org)** – Reusable 3D components in PyTorch from Meta FAIR. Differentiable rendering, mesh ops, and point-cloud primitives. [Docs](https://pytorch3d.readthedocs.io) | SDK: Python (pip install pytorch3d)
- **[NVIDIA GR00T](https://github.com/NVIDIA/Isaac-GR00T)** – NVIDIA's open humanoid foundation-model toolkit. Training recipes, policies, and data-generation pipelines for humanoids. [Docs](https://developer.nvidia.com/isaac-gr00t)
- **[GR00T-WholeBodyControl](https://nvlabs.github.io/GR00T-WholeBodyControl/)** – Unified platform for training and deploying humanoid whole-body controllers. Includes SONIC, a behavior foundation model trained on large-scale motion-capture data for walking, manipulation, and VR teleoperation. [Docs](https://github.com/NVlabs/GR00T-WholeBodyControl)

## Templates and Example Projects

> Reference implementations, demos, and starter projects.

- **[Isaac Lab Examples](https://github.com/isaac-sim/IsaacLabExtensionTemplate)** – Official template repo for building Isaac Lab tasks and training environments.
- **[LeRobot Tutorials](https://huggingface.co/docs/lerobot/en/tutorials)** – Step-by-step tutorials for recording robot data, training policies, and evaluating on real hardware.

---

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). One entry per PR — edit `entries.yaml` only and let the maintainers regenerate `README.md`.

## License

Released under [CC0 1.0 Universal](LICENSE). You may copy, modify, and redistribute without attribution.

## About Backblaze B2

[Backblaze B2 Cloud Storage](https://www.backblaze.com/cloud-storage) is S3-compatible object storage designed for AI and media workloads. This list is maintained as part of our work making B2 a convenient storage layer for AI workflows.
