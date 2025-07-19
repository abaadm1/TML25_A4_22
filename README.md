# Trustworthy Machine Learning — Assignment 4  
### Explainability • SS 2025 • Team 22

This repository contains our complete solution for **Assignment # 04: Explainability**.  
All four tasks (Network Dissection, Grad‑CAM variants, LIME, and the comparison study) are implemented and documented here, along with the required reports and the parameter pickle for the leaderboard submission.


## Repository layout

| Path | Type | Purpose |
|------|------|---------|
| **`Deliverable 01.pdf`** | Report | 1‑page analysis of **Task 1 – Network Dissection** (concept statistics, visualisations, and discussion). |
| **`Deliverable 02.pdf`** | Report | 1‑page report for **Task 2 – Grad‑CAM / AblationCAM / ScoreCAM** results on the 10 ImageNet images. |
| **`Deliverable 03.pdf`** | Report | 1‑page report for **Task 3 – LIME** explanations on the same 10 images. |
| **`Deliverable 05.pdf`** | Report | 1‑page comparative study (**Task 4**) highlighting differences between Grad‑CAM and LIME (IoU, qualitative insights). |
| **`final_lime_params.pkl`** | Pickle | Dictionary of the tuned keyword‑arguments for `explain_instance` (one entry per image). Upload this file to the evaluation server at the end (`/lime` endpoint). |
| **`tml-assignment-04-task-1.ipynb`** | Notebook | End‑to‑end pipeline for **Task 1**: loads ResNet‑18 models, runs Network Dissection (via [CLIP‑disection](https://github.com/…)), gathers neuron‑concept statistics, and exports plots used in `Deliverable 01.pdf`. |
| **`tml-assignment-04-task-2.ipynb`** | Notebook | Implementation of **Task 2**: applies Grad‑CAM, AblationCAM, and ScoreCAM on each ImageNet image using `torchcam`/`grad-cam` library; saves heat‑maps for the report. |
| **`tml-assignment-04-task-3.ipynb`** | Notebook | Implementation of **Task 3**: prepares images, runs LIME with the tuned parameters, computes IoU versus Grad‑CAM masks, saves overlays, and serialises `final_lime_params.pkl`. |

Release Tag: https://github.com/abaadm1/TML25_A4_22/releases/tag/v1.0.0
