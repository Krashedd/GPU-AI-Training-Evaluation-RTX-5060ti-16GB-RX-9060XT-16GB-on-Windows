# GPU AI Training Evaluation: RTX 5060 Ti 16GB vs RX 9060 XT 16GB on Windows

This repository contains all source code, configuration files, and raw benchmarking results for the study titled **"A Comparative Evaluation of Consumer-Grade AMD and NVIDIA GPUs for Academic AI Training."** The project evaluates the NVIDIA RTX 5060 Ti and AMD RX 9060 XT across representative AI workloads using Windows 11, Visual Studio Code, CUDA 12.9, and the ROCm for Radeon on Windows Public Preview.

Repository link:  
https://github.com/Krashedd/GPU-AI-Training-Evaluation-RTX-5060ti-16GB-RX-9060XT-16GB-on-Windows

---

## Overview

Three widely used academic workloads were benchmarked:

• **ResNet-152** – Image classification (Oxford-IIIT Pet)  
• **DistilBERT** – NLP text classification (AG News 2K subset)  
• **YOLOv8n** – Object detection (COCO 5K subset)

Metrics recorded include throughput, total training time, VRAM usage, GPU utilization, power draw, performance per watt, and validation accuracy.



## System Configuration

CPU: Intel Core i7-12700  
Memory: 32 GB DDR4 ECC  
Storage: 2 × 1 TB WD Black SN850X (one per GPU environment)  
OS: Windows 11  
NVIDIA Stack: CUDA 12.9 + Python 3.11.10  
AMD Stack: ROCm for Radeon on Windows Public Preview + Python 3.12.10

Each GPU was tested in isolation with its own NVMe drive and clean software environment.

---

## Reproducing the Experiments

### 1. Create a Virtual Environment (IMPORTANT)

Separate virtual environments are required to avoid CUDA–ROCm conflicts.

#### **For NVIDIA (CUDA 12.9):**
Requires **Python 3.11.10**

#### **For AMD (ROCm Windows Preview):**
Requires **Python 3.12.10**

## Results

Raw benchmarking results are available in the `results/` directory:

• Combined Excel file (full_results.xlsx)  

Metrics include:  
- Training throughput  
- Total training time  
- VRAM usage  
- GPU utilization  
- Power draw  
- Performance per watt  
- Validation scores  

---

## Associated Publication

Please cite this repository if used for academic or benchmarking purposes:

**IEEE Style Citation:**

C. J. C. Cangco, "GPU Benchmarking Code for Academic AI Workloads,"  
GitHub repository, 2025. Available: https://github.com/Krashedd/GPU-AI-Training-Evaluation-RTX-5060ti-16GB-RX-9060XT-16GB-on-Windows.

---

## Notes

• ROCm support for Radeon GPUs on Windows is extremely new, with the public PyTorch preview released in September 2025.  
• CUDA kernels remain more mature on Windows, particularly for transformer attention operations.  
• This repository reflects realistic academic workflows with consumer hardware and Windows-based tooling.

---

## Contact

Mapúa University
cccangco@mymail.mapua.edu.ph

