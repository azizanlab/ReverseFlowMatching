<h1 align="center">Reverse Flow Matching</h1>

<p align="center">
  <b><a href="https://arxiv.org/abs/2601.08136">A Unified Framework for Online Reinforcement Learning with Diffusion and Flow Policies</a></b>
  <br><br>
  Zeyang Li &nbsp;·&nbsp; Sunbochen Tang &nbsp;·&nbsp; Navid Azizan
  <br>
  <i>Massachusetts Institute of Technology</i>
  <br><br>
  <b>ICML 2026 (Spotlight)</b>
</p>

---

## Installation

```bash
git clone https://github.com/zeyang23/ReverseFlowMatching.git
cd ReverseFlowMatching
conda env create -f environment.yaml
conda activate rfm
```

## Quick Start

Train RFM on `cheetah-run` with the default config:

```bash
python main.py
```

Pick a different algorithm or environment via `--override`:

```bash
python main.py --override algo=rfm --override env.name=walker-run
python main.py --override algo=sac --override env.name=finger-turn_hard
```

See [`run.sh`](run.sh) for an example sweep across DMC tasks.

## Algorithms

Supported: RFM, SAC, DQS, MaxEntDP, QSM, QVPO.

## Logging

Each run writes outputs under `logs/<env_name>/<algo>/<run_name>/`.

Weights & Biases logging is enabled when `logger.debug: false` and `logger.wandb_project` is set.

## Acknowledgements

This codebase builds on [Diffusion Q-Sampling](https://github.com/vineetjain96/Diffusion_Q_Sampling).

## Citation

```bibtex
@inproceedings{li2026reverse,
  title     = {Reverse Flow Matching: A Unified Framework for Online Reinforcement Learning with Diffusion and Flow Policies},
  author    = {Li, Zeyang and Tang, Sunbochen and Azizan, Navid},
  booktitle = {International Conference on Machine Learning},
  year      = {2026}
}
```
