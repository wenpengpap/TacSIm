<img width="1914" height="755" alt="figure1_overview" src="https://github.com/user-attachments/assets/7fbbca6a-7bf6-400c-9db9-b3737ed0cf53" />
<div align="center">

# TacSIm

### A Dataset and Benchmark for Football Tactical Style Imitation

**CVPR 2026** · **Peng Wen** · **Yuting Wang** · **Qiurui Wang**


<p>
  <a href="https://openaccess.thecvf.com/content/CVPR2026/html/Wen_TacSIm_A_Dataset_and_Benchmark_for_Football_Tactical_Style_Imitation_CVPR_2026_paper.html"><img src="https://img.shields.io/badge/Paper-CVPR%202026-2563eb?style=for-the-badge" alt="CVPR 2026 Paper"></a>
  <a href="https://drive.google.com/drive/folders/12UFZcP00x63cXDKqX22awFFnKomylhiP"><img src="https://img.shields.io/badge/Download-Dataset-18834f?style=for-the-badge" alt="Dataset"></a>
  <a href="https://www.kaggle.com/competitions/tacsim"><img src="https://img.shields.io/badge/Online-Benchmark-f59e0b?style=for-the-badge" alt="Online Benchmark"></a>
</p>

**From real-world football broadcasts to tactical imitation in virtual environments.**

[Overview](#overview) · [Highlights](#highlights) · [Dataset](#dataset) · [Benchmark](#benchmark) · [News](#news) · [Citation](#citation)

</div>

---

## Overview

**TacSIm** introduces a large-scale dataset and benchmark for **football tactical style imitation**. Unlike approaches that primarily optimize game outcomes (e.g., goals or win rates), TacSIm focuses on reproducing the **spatial organization and movement patterns** of real football teams.

Starting from English Premier League broadcast footage, the framework reconstructs the positions of **all 22 players and the ball** in a normalized pitch-coordinate system and supports tactical imitation in a virtual football environment.
<img width="1914" height="755" alt="figure1_overview" src="https://github.com/user-attachments/assets/0c150f0a-cbb6-4a1d-aa9d-9be63532ba79" />

<p align="center">
  <img src="assets/figure1_overview.png" alt="Figure 1: TacSIm overview from the CVPR 2026 paper" width="100%">
</p>
<p align="center"><em>Figure 1 (from our paper). Real match footage → pitch-coordinate reconstruction → multi-agent tactical imitation in simulation.</em></p>

## Highlights

| **140 matches** | **38,913 segments** | **~54 hours** | **22 players + ball** |
|:---:|:---:|:---:|:---:|
| 2024–25 Premier League | Annotated video segments | 194,565 seconds of selected footage | Reconstructed pitch coordinates |

- **Real-match tactical contexts:** Offensive, defensive, and transition phases annotated from broadcast footage.
- **Broadcast-to-pitch reconstruction:** In-camera position estimation and off-camera trajectory completion in a standardized coordinate system.
- **Real-to-virtual imitation:** A shared setting for studying coordinated multi-agent behavior using realistic match scenarios.
- **Standardized evaluation:** Spatial occupancy similarity and movement-vector similarity across grid scales and prediction horizons.

## Dataset

TacSIm is built from broadcast footage of **140 matches** from the **2024–2025 English Premier League** season. The dataset contains player and ball trajectories with tactical-phase annotations. As described in the paper, the train/validation/test partition is **match-disjoint** to reduce leakage across splits.

### Dataset statistics

| Split | Video segments | Duration (s) | Proportion |
|:--|--:|--:|--:|
| Training | 27,240 | 136,195 | 70% |
| Validation | 5,837 | 29,185 | 15% |
| Test | 5,836 | 29,185 | 15% |
| **Total** | **38,913** | **194,565** | **100%** |

### Download

- **Google Drive:** [Access the TacSIm dataset](https://drive.google.com/drive/folders/12UFZcP00x63cXDKqX22awFFnKomylhiP)
- **Baidu Netdisk:** [Access the TacSIm dataset](https://pan.baidu.com/s/1v2-x9JpoFZbDsetMghqAHw?pwd=7gah) (code: `7gah`)

## Benchmark

TacSIm measures how closely a model can reproduce real-world football dynamics in a virtual environment. At test time, the model receives the **initial positions of players and the ball** and predicts the subsequent sequence. Under the paper's evaluation protocol, **ball trajectories** are scored to assess tactical imitation.

The benchmark reports two complementary metrics:

| Metric | What it measures |
|:--|:--|
| **Spatial Occupancy Similarity** ($S_t$) | Overlap between real and predicted occupancy on a discretized football pitch. |
| **Movement Vector Similarity** ($S_v$) | Agreement of movement and activity patterns across the evaluation window. |

The paper evaluates **BC**, **CMIL**, **IRL**, **CoDAIL**, and **DRAIL** at different grid resolutions and **3 s / 5 s / 10 s** prediction horizons.

<p align="center">
  <a href="https://www.kaggle.com/competitions/tacsim"><img src="https://img.shields.io/badge/Kaggle-Open%20the%20Online%20Benchmark-20beff?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle benchmark"></a>
</p>

### Qualitative visualization

<p align="center">
  <img src="assets/figure3_visualization.png" alt="Figure 3: Comparison of real and virtual trajectories at different spatial grid resolutions" width="100%">
</p>
<p align="center"><em>Figure 3 (from our paper). Real vs. virtual trajectories at three spatial grid resolutions (15 × 10, 20 × 12, and 30 × 20).</em></p>

## News

- **2026.09** — TacSIm dataset made publicly available.
- **2026.06.04** — Paper published online.
- **2026.02.21** — TacSIm accepted to **CVPR 2026**.

## Citation

If TacSIm is useful for your research, please consider citing our paper:

```bibtex
@inproceedings{wen2026tacsim,
  title     = {TacSIm: A Dataset and Benchmark for Football Tactical Style Imitation},
  author    = {Wen, Peng and Wang, Yuting and Wang, Qiurui},
  booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  pages     = {20014--20023},
  year      = {2026}
}
```
---

<div align="center">
  <sub>Computer Vision · Sports Analytics · Multi-Agent Learning</sub>
</div>


