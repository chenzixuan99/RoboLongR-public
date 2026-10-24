# RoboLongR

**RoboLongR: Causally Consistent Rewards Teach Robots to Progressively Master Long-Horizon Manipulation**

[Project Website](https://Robo-LongR.github.io)

## Overview

RoboLongR is an offline-to-online framework that learns history-dependent rewards to guide long-horizon policy adaptation. It pursues causal consistency by aligning predicted progress with task prerequisites supported by execution history.

The framework combines:

- **Stage-order supervision and recurrent memory** to encourage prerequisite-sensitive progress estimates.
- **Two-round reward learning** to refine trajectory segments using predicted progress.
- **Stage-conditioned learning from behavior cloning to online reinforcement learning** to guide policy adaptation on new tasks.
- **Terminal-feedback reward correction** that uses all three failed rollouts after three consecutive high-scoring failures.

## Reported Results

| Evaluation | RoboLongR success rate | Improvement over the comparison baseline |
| --- | ---: | ---: |
| 18 long-horizon RLBench tasks excluded from reward pretraining | 31.8% | +9.2 percentage points |
| Four real-robot tasks | 57.5% | +32.5 percentage points |

Reward pretraining uses demonstrations from 88 RLBench tasks and Open-X Embodiment data. Downstream evaluation measures policy adaptation using target-task demonstrations and online interaction.

## Repository Status

This initial public version contains the project overview. Training and evaluation code, datasets, and model checkpoints are not included in this version.
