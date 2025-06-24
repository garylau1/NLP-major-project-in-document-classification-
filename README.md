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
| `filtered_dataset.json`        | Cleaned and manually annotated ground truth JSON for evaluation |
| `original_dataset_without_labels.json` | Raw OCR-extracted dataset without labels, used before annotation |
| `Our_result.ipynb` | We plot all results, and this notebook includes all graphs/tables of our models |
| `labeled_output.json` | Cleaned and manually annotated ground truth JSON for (Piiranha model) training and evaluation |
| `Piiranha_model.ipynb` | Notebook for testing Piiranha_model |
| `wrapped_by_class.json` | We covert the filtered_dataset.json into a format that suits for Piiranha model training |
## 🧪 Models Compared

| Model               | Accuracy | F1 Score | Latency (s) | Notes                                  |
|--------------------|----------|----------|-------------|----------------------------------------|
| **Piiranha-v1**     | **99.2%**| **95.6%**         | **0.029**       | Baseline fine-tuned model      |
| **LLaMA 4 Maverick**     | **87.1%**| **86.6%**    | **1.038**       |              |
| **Claude 3.7**     | **99.44%** | **95.6%**  | **4.844**          |              
| **Deepseek-R1**     | -        | –        | –           | It fails to give structured output              |




## How to Use 🚀

### 1. Environment Setup
1. Install **Python 3.10**.  
2. Install dependencies:
   ```bash
   pip install \
  boto3==1.38.42 \
  awscli==1.40.40 \
  pandas==2.3.0 \
  matplotlib==3.10.3 \
  pydantic==2.10.0
### 2. The way to use the notebooks and files to replicate the results
1. Open any of the testing notebooks to evaluate specific LLMs/Piiranha-v1:
   - `claude_testing.ipynb`
   - `llama_4_testing.ipynb`
   - `deepseek_testing.ipynb`
   - `Piiranha-v1`
2. View dataset insights and preprocessing:
   - `Dataset_Visualization&Stats.ipynb`

3. Evaluate model predictions using `filtered_keys_edit11 1.json` as ground truth.

4. Train and evaluate model Piiranha-v1 using `labeled_output.json` as ground truth.

5. We compare and plot our results using `Our_result.ipynb`
