# brain-tumor-segmentation-research-proposal
Hybrid CNN–Transformer Architecture with Dual Attention Mechanisms

This repository contains the research proposal titled:

“Multi-Modal MRI-Based Brain Tumor Segmentation Using Integrated CNN, Transformer, and Attention Modules”
by Md. Shahidul Islam Shabuz,
Faculty of Computer Science & Information Technology,
University of Malaya (UM), Kuala Lumpur.

The proposal document is included here for academic visibility and future code implementation.
The method integrates CNN + Swin Transformer + Spatial Attention + Channel Attention with Cross-Attention Fusion to address challenges in medical image segmentation.

Abstract Summary

This research proposes a hybrid deep learning model for segmenting brain tumor subregions in multi-modal MRI using:

CNN Encoder (ResNet-50) → Local spatial feature extraction

Swin Transformer Backbone → Global context modeling

Spatial Attention Module → Enhances boundary localization

Channel Attention Module → Learns modality-specific importance

Cross-Attention Fusion Layer → Merges CNN + Transformer features

Hybrid Loss (Dice + Focal Loss) → Handles class imbalance

Patch-based and mixed-precision training → Efficient computation

The method is evaluated on BraTS 2023 and TCIA Glioma datasets using metrics such as Dice, HD95, ASD, Sensitivity, Specificity, and inference time.

Key Research Objectives
RO1: Review current deep learning approaches for brain tumor segmentation
RO2: Propose a hybrid model addressing class imbalance and spatial complexity
RO3: Develop the model using CNN, Transformer, and attention blocks
RO4: Evaluate the model across multi-institutional MRI datasets

Why This Research Matters

Tumor tissues often have low contrast, irregular shapes, and unclear boundaries.

CNNs excel at local details; Transformers excel at global context.

Attention helps identify relevant tumor regions and important MRI modalities.

The proposed architecture improves accuracy, boundary precision, and generalization.

Proposed Architecture
Components:

ResNet-50 Encoder

Swin Transformer Blocks

Spatial & Channel Attention

Cross Attention Fusion (CAF)

U-Net-style Decoder

Combined Dice + Focal Loss

Designed to solve:

Class imbalance

Boundary inaccuracy

Domain shift (BraTS → TCIA)

High computational cost

 Datasets
1. BraTS 2023

T1, T1c, T2, FLAIR

Labels: ET, ED, NCR/NET

2. TCIA Glioma Collection

Used for external validation

Multiple institutions and scanners

Evaluation Metrics

Dice Similarity Coefficient (DSC)

HD95 (95% Hausdorff Distance)

Average Surface Distance (ASD)

Sensitivity & Specificity

Inference Time per Slice

Planned Implementation (Coming Soon)

This repository will later include:

✔ Preprocessing pipelines (Skull stripping, N4 bias correction)

✔ Model architecture scripts

✔ Training & validation code

✔ TensorBoard logs

✔ Evaluation notebooks
