# CLAUDE.md — awesome-physical-ai

## What this list is

A curated directory of tools for **physical AI** — robotics and embodied AI systems: vision-language-action models, world models, physics simulators, learning frameworks, real-world middleware, and data-collection hardware.

## Scope

**Include**
- Robotics foundation models (VLAs, generalist policies, humanoid models).
- Generative world models for physical simulation and planning.
- Physics simulators and training environments (Isaac, MuJoCo, Genesis, Gazebo).
- Robot-learning frameworks (imitation learning, RL, BC).
- Public datasets and benchmarks for embodied AI.
- Robot middleware and runtime (ROS 2, Dora).
- Open teleop hardware and data-collection software.
- 3D / perception / kinematics SDKs relevant to robotics.
- Template/demo projects and tutorials.

**Exclude**
- General-purpose ML tools — those belong in `awesome-ml-data-pipelines` or `awesome-multimodal-data`.
- Pure LLM agent frameworks — those belong in `awesome-agent-infrastructure`.
- Research papers without runnable code or usable weights.
- Closed humanoid platforms without developer access.

**Inclusion requirements (every entry)**
- Public product, docs, or code; URL resolves.
- Activity signal within the last 12 months.
- Either open weights, an open-source codebase, or a clear developer-access path.

## Files, schema, workflow, rules

Identical to the rest of the awesome-* family. See `~/awesome-lists/CLAUDE.md` for the global workflow and `~/awesome-lists/_shared/schema.json` for field definitions. Per-repo reminders:

- Edit `entries.yaml` only. `README.md` and `llms.txt` are generated.
- `b2_integration` is a URL to B2 docs, or `""` if none.
- Never delete an entry; tag `needs-review` and log a note in `~/awesome-lists/_tasks/`.
