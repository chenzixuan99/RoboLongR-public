# RoboLongR

**RoboLongR: Causally Consistent Rewards Teach Robots to Progressively Master Long-Horizon Manipulation**

[Project Website](https://chenzixuan99.github.io/RoboLongR-public/) · [Paper](assets/robolongr-paper.pdf) · [Project Video](assets/robolongr-video.mp4)

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

This public repository contains the project website, research figures, paper PDF, and demonstration video. Training and evaluation code, datasets, and model checkpoints are not included in this version.

## Website

The website is served by GitHub Pages from the root of the `main` branch. All figures, the paper, and the video are included under `assets/`.

Website content was migrated from [Robo-LongR/robo-longr.github.io](https://github.com/Robo-LongR/robo-longr.github.io) at commit `3649120395b526895e02bf2a4da399e41ba95511`. This public version removes the website's anonymous labels, enables search indexing, and uses this repository's project URL. The author list is not displayed yet.
