# 🔐 PII Detection in ID Documents using LLMs

This is a major project for **COMP8420 – Advanced Natural Language Processing**, focused on enhancing identity verification systems by detecting and classifying **Personally Identifiable Information (PII)** and **non-PII** from OCR-extracted text in Australian driver's licenses using state-of-the-art **Large Language Models (LLMs)**.

---

## 🚀 Project Overview

With the rise of identity fraud, accurate classification of PII in ID documents is critical. This project benchmarks and fine-tunes several LLMs (Claude, LLaMA 4 Maverick, DeepSeek, Piiranha-v1) to improve both **accuracy** and **latency** in text extraction pipelines.

---

## 📁 Dataset

- **464** real-world Australian driver's licenses
- Extracted using OCR and **pseudonymized** to protect privacy
- Each sample is manually annotated for **PII** and **non-PII** fields

---

## 📂 Repository Structure

| File/Folder                           | Description |
|--------------------------------------|-------------|
| `README.md`                          | Project overview and documentation |
| `claude_testing.ipynb`               | Notebook for testing Claude model's performance on OCR text |
| `llama_4_testing.ipynb`              | Notebook for testing LLaMA 4 Maverick model |
| `deepseek_testing.ipynb`             | Notebook for testing DeepSeek model (includes formatting challenges) |
| `Dataset_Visualization&Stats.ipynb`  | Notebook for preprocessing, cleaning, and visualizing dataset distribution |
| `filtered_keys_edit11 1.json`        | Cleaned and manually annotated ground truth JSON for evaluation |
| `original_dataset_without_labels.json` | Raw OCR-extracted dataset without labels, used before annotation |




## 🧪 Models Compared

| Model               | Accuracy | F1 Score | Latency (s) | Notes                                  |
|--------------------|----------|----------|-------------|----------------------------------------|
| **Piiranha-v1**     | **99.44%** | –        | –           | Baseline fine-tuned model              |
| **LLaMA 4 Maverick**| 87.3%    | 86.6%



## ▶️ How to Use

1. Open any of the testing notebooks to evaluate specific LLMs:
   - `claude_testing.ipynb`
   - `llama_4_testing.ipynb`
   - `deepseek_testing.ipynb`

2. View dataset insights and preprocessing:
   - `Dataset_Visualization&Stats.ipynb`

3. Evaluate model predictions using `filtered_keys_edit11 1.json` as ground truth.
