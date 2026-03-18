# Edge AI Drone Detection

**Preprint** | Submitted to the AI Research Conference (AIRC)

---

## Abstract

This paper presents a lightweight, real-time drone detection system designed for deployment on resource-constrained edge devices. As unmanned aerial vehicles (UAVs) become increasingly prevalent, rapid and accurate detection is critical for security, privacy, and airspace management. We propose an optimized inference pipeline that combines a compact convolutional neural network (CNN) backbone with hardware-aware post-training quantization, enabling sub-50 ms latency on embedded platforms such as the NVIDIA Jetson Nano and Raspberry Pi 4. Evaluated on a multi-source UAV dataset, our approach achieves a mean average precision (mAP) of **91.3%** at IoU 0.5 while reducing model size by 4× compared to a full-precision baseline. These results demonstrate that high-accuracy drone detection is achievable at the edge without reliance on cloud connectivity.

---

## Paper

📄 **[Read the Preprint (PDF)](./paper/edge_ai_drone_detection_preprint.pdf)**

---

## Citation

If you use this work, please cite:

```bibtex
@article{tambevarad2026edgeai,
  title     = {Edge AI Drone Detection: Real-Time UAV Detection on Resource-Constrained Devices},
  author    = {Tambe, Varad},
  journal   = {Preprint — Submitted to AI Research Conference (AIRC)},
  year      = {2026},
  url       = {https://github.com/tambevarad/edge-ai-drone-detection}
}
```

---

## Overview

| Property | Value |
|---|---|
| Task | UAV / Drone Detection |
| Backbone | MobileNetV3-Small + SSD Head |
| Quantization | INT8 post-training quantization |
| Target Hardware | NVIDIA Jetson Nano, Raspberry Pi 4, OAK-D |
| Framework | PyTorch · TensorRT · ONNX Runtime |
| Dataset | VisDrone2019 + custom flight footage |
| mAP@0.5 | 91.3% |
| Latency (Jetson Nano) | 43 ms per frame |
| Model Size | 4.2 MB (INT8) |

---

## Key Contributions

1. **Quantization-Aware Pipeline** – End-to-end INT8 quantization workflow that preserves detection accuracy while cutting memory footprint by 75%.
2. **Edge-Optimized Architecture** – Depthwise-separable convolutions and pruned anchor sets tailored for drone aspect ratios.
3. **Multi-Source Dataset Fusion** – Augmented training corpus combining aerial surveillance footage with synthetically rendered UAV scenes for improved generalisation.
4. **Benchmark Suite** – Reproducible evaluation harness measuring mAP, latency, and power draw across three hardware targets.

---

## Repository Structure

```
edge-ai-drone-detection/
├── paper/
│   └── edge_ai_drone_detection_preprint.pdf   # Preprint manuscript
├── README.md
```

---

## Contact

**Varad Tambe** — [GitHub](https://github.com/tambevarad)

*Pre-print submitted to the AI Research Conference (AIRC). All rights reserved.*
