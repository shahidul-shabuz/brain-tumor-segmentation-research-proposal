# Multi-Modal MRI Brain Tumor Segmentation with an Integrated CNN, Transformer and Attention Method

**Status: research proposal. No code or results yet.**

Brain tumor sub-regions in multi-modal MRI are hard to segment: tumor tissue has low contrast and irregular boundaries, the classes are heavily imbalanced, and models trained on one dataset often degrade on scans from other institutions. This proposal designs a hybrid method that combines a CNN encoder (local detail), a Swin Transformer (global context), spatial and channel attention, and cross-attention fusion. It is to be trained with a Dice + Focal loss and evaluated on BraTS 2023, with external validation on TCIA glioma data.

## About this proposal

| | |
|---|---|
| **Document** | [`Research_Proposal Shabuz.pdf`](Research_Proposal%20Shabuz.pdf) |
| **Prepared** | 2025, as a postgraduate research proposal for the Faculty of Computer Science and Information Technology, Universiti Malaya, Kuala Lumpur |
| **Proposed supervisors** | Prof. Dr. Por Lip Yee; Madam Fazidah binti Othman (Universiti Malaya) |
| **Current status** | I did not continue at Universiti Malaya. The topic remains one of my research interests, and I plan to implement the method here. |

## Research objectives

- **RO1:** Review current deep learning approaches to brain tumor segmentation in multi-modal MRI.
- **RO2:** Propose a hybrid method that addresses class imbalance and spatial complexity.
- **RO3:** Implement the method from CNN, Transformer and attention components.
- **RO4:** Evaluate it across multi-institutional MRI datasets.

## Proposed method

| Component | Role |
|---|---|
| ResNet-50 CNN encoder | Local spatial features |
| Swin Transformer blocks | Global context |
| Spatial attention | Sharper tumor-boundary localisation |
| Channel attention | Learns how much each MRI modality matters |
| Cross-attention fusion | Merges CNN and Transformer features |
| U-Net-style decoder | Restores full-resolution masks |
| Dice + Focal loss | Handles class imbalance between tumor sub-regions and background |
| Patch-based, mixed-precision training | Keeps memory and compute manageable |

## Planned data

- **BraTS 2023 (adult glioma):** T1, T1c, T2 and FLAIR. Labels: enhancing tumor (ET), edema (ED), necrotic/non-enhancing core (NCR/NET). Main training and evaluation set.
- **TCIA glioma collections:** external validation across institutions and scanners.

No MRI or patient data will be stored in this repository. Both datasets must be obtained from their official sources under their own terms of use.

## Planned evaluation

- Dice similarity coefficient
- 95th-percentile Hausdorff distance (HD95)
- Average surface distance (ASD)
- Sensitivity and specificity
- Inference time per slice

## Planned implementation

- [ ] Preprocessing: skull stripping, N4 bias-field correction, intensity normalisation
- [ ] Data loaders with patient-level train/validation/test splits
- [ ] Baseline U-Net with Dice, HD95 and ASD evaluation
- [ ] Hybrid CNN–Swin model with attention and cross-attention fusion
- [ ] Training and evaluation scripts, fixed seeds, configuration files
- [ ] Results and segmentation figures (from actual runs only)

## Contact

Md. Shahidul Islam Shabuz · Assistant Professor, Dept. of CSE, Rajshahi Science and Technology University (RSTU)
[Website](https://shahidul-shabuz.github.io/) · [Google Scholar](https://scholar.google.com/citations?user=VDtX90sAAAAJ&hl=en) · [ORCID](https://orcid.org/0009-0008-8271-888X) · shahidul.shabuz@gmail.com
