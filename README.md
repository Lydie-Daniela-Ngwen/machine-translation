# Machine Translation Project

## 📌 Project Overview

This project explores the use of different language models for **machine translation (English → French)** and evaluates their performance using standard automatic metrics.

The objectives are:
- Apply different types of models to a translation task  
- Compare their performance  
- Evaluate translation quality using automatic metrics  

Three models are used:
- **Helsinki-NLP/opus-mt-en-fr** (sequence-to-sequence)  
- **google/flan-t5-large** (sequence-to-sequence)  
- **openai/gpt-oss-120b** (autoregressive model)  

---

## ⚙️ Workflow

### 1. Data Sampling
- A dataset of sentence pairs (English–French) is loaded (`sents.csv`)  
- A random sample of **20 sentences** is selected  
- The sample is saved as a new CSV file  

### 2. Translation
- Each model translates English sentences into French  
- Tokenization and generation are handled using **Hugging Face Transformers**  
- Outputs are stored alongside reference translations  

### 3. Preprocessing
- Reference translations are cleaned (e.g., removal of non-breaking spaces)  
- Data is structured for evaluation  

### 4. Evaluation

Translations are evaluated using three types of automatic metrics:

- **Edit-based metric**
  - WER (Word Error Rate)

- **N-gram-based metric**
  - BLEU

- **Semantic similarity metric**
  - BERTScore  

### 5. Model Comparison
- Performance of the three models is compared  
- Results are analyzed across metrics  
- A normalized aggregate score is computed  

---

## 🧠 Key Insights

- Automatic evaluation provides a **consistent and scalable alternative** to human evaluation  
- Different models perform differently depending on the metric  
- Semantic metrics (e.g., BERTScore) better capture meaning than surface-level metrics  

---

## 🛠️ Technologies Used

- Python  
- Hugging Face Transformers  
- Pandas  
- BERTScore  
- Evaluation metrics: WER, BLEU  

---

## 📂 Files

- `sents.csv` – original dataset  
- `sents_sample_20.csv` – sampled dataset  
- Notebook – full pipeline (sampling, translation, evaluation)  

---

## 🚀 How to Run

```bash
pip install transformers pandas bert-score
