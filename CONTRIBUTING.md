# Contributing

Thanks for your interest in contributing. This list covers open-source tools for physical AI and robotics; small, careful PRs keep it useful.

## How to contribute

1. Fork this repo.
2. Edit **`entries.yaml`** only. Do not edit `README.md` or `llms.txt` — those are regenerated.
3. Place your entry in the appropriate category (see `categories.yaml`).
4. Open a PR. One entry per PR.

## What belongs in the list

**We accept**
- Robotics foundation models (VLAs, generalist policies).
- World models and physics-aware generative systems.
- Physics simulators and training environments.
- Robot-learning frameworks and RL libraries.
- Datasets and benchmarks for embodied AI.
- Robot middleware and runtime.
- Open teleop hardware and data-collection tooling.
- 3D / perception SDKs and demos.

**We don't accept**
- General-purpose ML infra (see `awesome-ml-data-pipelines`).
- Pure LLM agent tools (see `awesome-agent-infrastructure`).
- Research papers without code or usable weights.
- Closed platforms without developer access.

## Inclusion requirements

- Public product, docs, or code; URL resolves.
- Activity signal within the last 12 months.
- Open weights, open source, or a clear developer-access path.

## Entry format

```yaml
- name: HuggingFace LeRobot
  url: https://github.com/huggingface/lerobot
  docs_url: https://huggingface.co/docs/lerobot
  description: End-to-end robot-learning library from HuggingFace.
  category: robot-learning-frameworks
  github: huggingface/lerobot
  license: Apache-2.0
  sdks:
    - {language: Python (pip install lerobot)}
  b2_integration: ""
  last_verified: 2026-04-17
```

Field reference is identical across all awesome-* lists in this family.

## Code of conduct

This project follows standard open-source community norms. Be kind, be constructive, focus on the contribution.
