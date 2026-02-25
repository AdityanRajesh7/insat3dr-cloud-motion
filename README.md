# INSAT-3DR Cloud Motion Forecasting

## Overview

Accurate short-term cloud motion forecasting remains challenging due to the limitations of optical flow and deterministic CNN models, which often produce blurry outputs and fail to capture uncertainty in rapidly evolving weather systems.

This project explores:

- Deterministic UNet-based forecasting
- Conditional Diffusion-based probabilistic forecasting

using multispectral INSAT-3DR/3DS Level-1C satellite imagery (VIS, IR, WV).

---

## Dataset

Source: MOSDAC (INSAT-3DR / 3DS)

Input:
- 4–6 past frames (multispectral)

Output:
- 1–2 future frames

Data is parsed from HDF5, normalized, and structured into spatio-temporal sequences.

---

## Models

### 1. UNet Baseline
- Encoder-decoder CNN
- Skip connections
- Multi-channel input
- Predicts future cloud frames directly

### 2. Diffusion Model
- Conditional denoising diffusion probabilistic model (DDPM)
- Timestep embeddings
- UNet backbone
- Learns probabilistic cloud evolution

---

## Author

Adityan Rajesh  
Artificial Intelligence & Data Science  
Amrita Vishwa Vidyapeetham

---

## License

MIT