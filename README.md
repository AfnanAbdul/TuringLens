# TuringLens: Detecting AI-Generated Academic Writing

TuringLens is a project for detecting AI-generated text in **academic writing**, such as essays and research abstracts. The project fine-tunes and evaluates several language models to identify AI-authored content and reduce false positives on human writing.

---

## What It Does

- Fine-tunes LLMs (e.g. RoBERTa, GPT-2) on **student essays**  
- Evaluates performance on **academic abstracts** from RAID  

---

## 📁 Datasets Used

### 📘 Kaggle LLM Dataset
- ~29,000 student essays (human vs. GPT-3.5-generated)  
- Used for initial model training  
- Lightweight and well-labeled for fast fine-tuning  

### 🧪 RAID (Robust AI Text Detection)
- 10M+ samples from 11 LLMs across 11 domains  
- Our subset focused on **academic abstracts**  
- Includes **adversarial examples** (e.g. typos, paraphrasing)

---

## 📊 Results

| Model           | Human Accuracy | AI Accuracy | Overall Accuracy |
|----------------|----------------|-------------|------------------|
| RoBERTa-base    | 95.5%          | 99.8%       | 97.2%            |
| GPT-2           | 95.5%          | 99.8%       | 97.2%            |
| **RoBERTa-LoRA** | **99.5%**      | **99.8%**   | **99.6%**        |

> 📉 On RAID, RoBERTa-LoRA reduced human false positives from **83.2% → 0.7%**

---

## 📌 Future Work

- 📊 **Benchmark against tools** like GPTZero, Turnitin  
- 🧠 **Add stylometric features** (e.g., sentence complexity, lexical variety)  
- 📉 **Use predictability metrics** like perplexity & burstiness  
- 🧾 **Measure vocabulary richness** (e.g., TTR, Hapax Legomenon Rate)

---
