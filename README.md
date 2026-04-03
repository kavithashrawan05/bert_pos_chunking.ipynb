# bert_pos_chunking.ipynb

## 📌 Overview
This project demonstrates how to fine-tune a transformer model (BERT) for token classification tasks:
- Part-of-Speech (POS) Tagging
- Chunking (Phrase Detection)

The model is trained using the CoNLL-2003 dataset and implemented using Hugging Face Transformers.

## 🎯 Objective
To build a token classification system that can:
- Assign grammatical tags (POS)
- Detect phrase-level chunks in sentences

## 🛠️ Technologies Used
- Python
- Hugging Face Transformers
- Datasets Library
- PyTorch
- Jupyter Notebook

---

## 📂 Dataset
- **CoNLL-2003 Dataset**
- Contains:
  - Tokens
  - POS Tags
  - Chunk Tags
  - Named Entity Tags

---

## ⚙️ Workflow
Raw Data → Tokenization → Label Alignment → Model Training → Evaluation → Inference

## 🔧 Key Steps

### 1. Tokenization
- Used BERT tokenizer
- Handled subword tokenization

### 2. Label Alignment
- Aligned labels with tokens
- Used `-100` for special tokens

### 3. Model
- Used `bert-base-cased`
- AutoModelForTokenClassification

### 4. Training
- Learning Rate: 2e-5
- Epochs: 2
- Batch Size: 16

### 5. Evaluation
- Metric: SeqEval
- Evaluated using:
  - Precision
  - Recall
  - F1 Score

## 📊 Results
The model successfully learned:
- POS tagging (grammar-level understanding)
- Chunking (phrase-level grouping)

## 🔍 Inference Example

Input:
John works at Google in California

Output:
- John → NNP
- works → VBZ
- Google → NNP
- California → NNP

## ⚠️ Challenges Faced
- Handling subword tokenization
- Aligning labels with tokens
- Dataset compatibility issues

## 💡 Conclusion
This project highlights how transformer models like BERT can effectively perform token classification tasks with high accuracy and contextual understanding.
