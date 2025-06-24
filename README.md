PII Detection in ID Documents using LLMs
A major project for COMP8420 – Advanced Natural Language Processing, aiming to enhance identity verification by detecting and classifying Personally Identifiable Information (PII) and non-PII in OCR-extracted text from Australian driver's licenses using state-of-the-art Large Language Models (LLMs).

🚀 Project Overview
With rising identity fraud, accurate classification of PII in ID documents is critical. This project benchmarks and fine-tunes several advanced LLMs (Claude, LLaMA 4 Maverick, DeepSeek, Piiranha-v1) to improve both accuracy and speed of text extraction pipelines in ID verification systems.

📁 Dataset
319 real-world Australian driver’s licenses

Extracted via OCR and pseudonymized to preserve privacy

Manually annotated ground truth for both PII and non-PII fields

Covers diverse states and license classes (ACT, NSW, QLD, VIC, TAS)

Methodology
OCR Extraction: Raw text extracted from ID document images

Manual Ground Truth Mapping: JSON mapping of PII/non-PII from OCR lines

Model Benchmarking: Evaluate LLMs on:

Accuracy (Precision, Recall, F1-Score)

Latency (mean inference time)

Cloud Integration: Models deployed and tested using AWS Bedrock to handle large-scale inference

⚙️ Technologies
Python 3.10+

AWS Bedrock for LLM inference

OCR preprocessing pipeline

Custom evaluation metrics (set-based F1/Precision/Recall comparison)

Pandas, NumPy, Matplotlib for analysis

📌 Key Findings
DeepSeek is unusable due to narrative-style outputs unsuitable for structured JSON parsing.

LLaMA 4 Maverick outperforms Claude in latency while maintaining comparable accuracy.

OCR quality significantly impacts performance, especially on low-resolution or noisy scans.

Future improvements include better OCR engines, image preprocessing, and feedback-driven dataset refinement.
