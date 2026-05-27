# Epilepsy SOZ Classification using DistilBERT and Whisper

## Overview

This project explores the use of Artificial Intelligence, Natural Language Processing (NLP), and Speech-to-Text technologies to classify possible Seizure Onset Zones (SOZ) from patient-reported epilepsy symptoms.

The system combines:

- DistilBERT for text classification
- OpenAI Whisper for speech transcription
- HuggingFace Transformers
- PyTorch deep learning framework

The goal is to analyze patient language patterns and predict possible seizure onset regions from written or spoken symptom descriptions.

---

# Features

- NLP-based epilepsy symptom classification
- Speech-to-Text transcription using Whisper
- SOZ prediction from patient descriptions
- HuggingFace Trainer pipeline
- Train / Validation / Test dataset splitting
- Automatic tokenization and preprocessing
- Performance evaluation with classification metrics
- Audio recording directly in Google Colab

---

# Technologies Used

- Python
- PyTorch
- HuggingFace Transformers
- DistilBERT
- OpenAI Whisper
- Scikit-learn
- Pandas
- NumPy
- Google Colab

---

# Project Workflow

```text
Patient Speech/Text
        ↓
Speech-to-Text (Whisper)
        ↓
Text Preprocessing
        ↓
DistilBERT Tokenization
        ↓
SOZ Classification
        ↓
Predicted Seizure Onset Zone
```

---

# Dataset

The dataset contains epilepsy patient symptom descriptions associated with different Seizure Onset Zones (SOZ).

### Dataset Fields

- `Patient_Expression`
- `SOZ`

### Dataset Size

- Approximately 400 samples

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/yourrepository.git
cd yourrepository
```

Install dependencies:

```bash
pip install transformers datasets torch scikit-learn pandas
pip install --upgrade transformers
pip install git+https://github.com/openai/whisper.git
```

Install FFmpeg:

```bash
apt-get install ffmpeg
```

---

# Model Architecture

## NLP Model

- `distilbert-base-uncased`

## Speech-to-Text Model

- `Whisper base`

---

# Data Processing

The pipeline includes:

- Missing value removal
- Label encoding
- Dataset stratification
- HuggingFace dataset conversion
- Tokenization with maximum sequence length of 128

---

# Training Configuration

| Parameter | Value |
|---|---|
| Epochs | 5 |
| Learning Rate | 1e-5 |
| Batch Size | 4 |
| Max Sequence Length | 128 |
| Weight Decay | 0.01 |
| Warmup Ratio | 0.1 |

---

# Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score

Example:

```python
print(classification_report(y_true, y_pred))
```

---

# Example Predictions

### Example 1

Input:

```text
"It happens during night"
```

Prediction:

```text
[Predicted SOZ]
```

### Example 2

Input:

```text
"I feel dizzy"
```

Prediction:

```text
[Predicted SOZ]
```

---

# Speech-to-Text Integration

The project includes a complete Speech-to-Text pipeline:

1. Audio recording from the browser
2. Audio transcription using Whisper
3. Automatic SOZ prediction from spoken symptoms

---

# Future Improvements

- Increase dataset size
- Improve class balance
- Fine-tune larger transformer models
- Add multilingual support
- Deploy as a web application
- Add confidence scores and explainability
- Explore medical-domain language models

---

# Ethical Disclaimer

This project is intended for research and educational purposes only.

It is not designed for clinical diagnosis, medical treatment, or healthcare decision-making.

---

# Project Structure

```text
├── data/
├── notebooks/
├── models/
├── results/
├── README.md
├── requirements.txt
```

---

# Author

Your Name

---

# License

MIT License
