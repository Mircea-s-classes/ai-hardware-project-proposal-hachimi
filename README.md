[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/v3c0XywZ)
# AI Hardware Project - HLS-CNN-MNIST
ECE 4332 / ECE 6332 — AI Hardware  
Fall 2025

## 🧭 Overview
This project builds a hardware accelerator for a convolutional neural network (CNN) on the PYNQ-Z2 platform. The accelerator is written in C++ and synthesized to RTL with High-Level Synthesis (HLS). It targets MNIST digit classification with 8-bit quantized inputs and weights to reduce memory bandwidth and improve throughput.

The design exposes the CNN as a reusable IP core in the PL (FPGA fabric in the ZYNQ7020 SOC). The PS (ARM cores in the ZYNQ7020 SOC) run a PYNQ Python overlay that controls the IP via AXI4-Lite and moves data via AXI DMA (AXI4-Stream) between DRAM and the accelerator. A 28×28 grayscale image (int8) is streamed to the IP; the IP computes the forward propagation and streams out the predictions back to PS via AXI DMA.

## 🗂 Folder Structure
- `docs/` – project proposal and documentation  
- `presentations/` – midterm and final presentation slides  
- `report/` – final written report (IEEE LaTeX and DOCX versions included)  
- `src/` – source code for software, hardware, and experiments  
- `data/` – datasets or pointers to data used

## 🧑‍🤝‍🧑 Team Setup
- Junting Huo

## 📋 Required Deliverables
1. **Project Proposal** — due Nov. 5, 2025, 11:59 PM  
2. **Midterm Presentation** — Nov. 19,2025, 11:59 PM  
3. **Final Presentation and Report** — Dec. 17, 11:59 PM

## 🚀 How to Use This Template
1. Click **“Use this template”** on GitHub.  
2. Name your repo `ai-hardware-teamXX` (replace XX with your team name or number).  
3. Clone it locally:
   ```bash
   git clone https://github.com/YOUR-ORG/ai-hardware-teamXX.git
   ```
4. Add your work in the appropriate folders.

## 🧾 Submissions
- Commit and push all deliverables before each deadline.
- Tag final submissions with:
   ```bash
   git tag v1.0-final
   git push origin v1.0-final
   ```

## 📜 License
This project is released under the MIT License.
