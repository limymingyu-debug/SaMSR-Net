# SaMSR-Net
SaMSR-Net： A Sample-Adaptive Multi-Scan Routing Mamba Network for Water Body Extraction
**SaMSR-Net: A Sample-Adaptive Multi-Scan Routing Mamba Network for Water Body Extraction**

## Overview

SaMSR-Net is a hybrid CNN–Mamba framework for water body extraction from Sentinel-2 imagery. It combines sample-adaptive multi-scan routing with boundary-aware attention to model spatial context and refine water–land boundaries.

## Method

The network includes two main modules:

- **MSR-VSS** uses a pool of 16 predefined scanning experts and sample-adaptive Top-K routing. The default configuration activates 8 experts.
- **DOBA** combines channel attention with spatial attention informed by Scharr and Laplacian responses to refine skip features.

The default architecture uses convolutional blocks at the two shallower feature levels and MSR-VSS blocks at the three deeper levels.

## Input Data

The model uses 13 input channels:

| Channel | Description |
|---|---|
| B2 | Blue |
| B3 | Green |
| B4 | Red |
| B8 | Near infrared |
| B8A | Narrow near infrared |
| B5 | Red edge |
| B6 | Red edge |
| B7 | Red edge |
| B11 | Short-wave infrared |
| B12 | Short-wave infrared |
| MNDWI | Modified Normalized Difference Water Index |
| AWEI_sh | Automated Water Extraction Index for shadow conditions |
| SLOPE | Terrain slope |

Bands and auxiliary layers are spatially aligned to a common grid before model input. The channel listing above describes the inputs; the required tensor channel order will be documented with the released preprocessing code.

## Study Area

The experiments described in the manuscript use Sentinel-2 imagery from Anhui Province, China.

## Repository Status

This repository is being prepared. Source code, model weights, and dataset files have not yet been uploaded.

Data access instructions, preprocessing details, dataset splits, and training and evaluation commands will be documented alongside the corresponding files when available.

## Publication and Citation

Publication details and citation information will be added when available.
