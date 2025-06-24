# 🔐 PII Detection in ID Documents using LLMs

This is a major project for **COMP8420 – Advanced Natural Language Processing**, focused on enhancing identity verification systems by detecting and classifying **Personally Identifiable Information (PII)** and **non-PII** from OCR-extracted text in Australian driver's licenses using state-of-the-art **Large Language Models (LLMs)**.

---

## 🚀 Project Overview

With the rise of identity fraud, accurate classification of PII in ID documents is critical. This project benchmarks and fine-tunes several LLMs (Claude, LLaMA 4 Maverick, DeepSeek, Piiranha-v1) to improve both **accuracy** and **latency** in text extraction pipelines.

---

## 📁 Dataset

- **319** real-world Australian driver's licenses
- Extracted using OCR and **pseudonymized** to protect privacy
- Each sample is manually annotated for **PII** and **non-PII** fields

---

## 🧪 Models Compared

| Model               | Accuracy | F1 Score | Latency (s) | Notes                                  |
|--------------------|----------|----------|-------------|----------------------------------------|
| **Piiranha-v1**     | **99.44%** | –        | –           | Baseline fine-tuned model              |
| **LLaMA 4 Maverick**| 87.3%    | 86.6%
