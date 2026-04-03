# Multimodal Emotion Recognition in Conversations 🎭🧠

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![University of Michigan](https://img.shields.io/badge/UMich-00274C?style=flat)](https://umich.edu)

> **SemEval 2024 Task 3 — Multimodal Emotion Cause Analysis in Conversations**  
> University of Michigan, Dearborn | Fall 2023

---

## Overview

This project tackles **emotion recognition in conversations** as part of the [SemEval 2024 Task 3](https://nustm.github.io/SemEval-2024-ECAC/) shared competition — a challenging NLP benchmark requiring systems to identify both the emotion expressed and its causal trigger across multi-turn dialogue.

The system explores a multimodal approach — combining **text-based NLP** and **audio feature analysis** — to classify emotions across conversational utterances. Multiple ML and deep learning architectures are evaluated and compared, with GloVe embeddings and hyperparameter optimization achieving a **15% accuracy improvement** over the baseline.

---

## Results

### Text Modality

| Model | Notes |
|---|---|
| Logistic Regression | Baseline |
| Naive Bayes | Fast, interpretable |
| Decision Tree | Feature importance analysis |
| Random Forest | Ensemble improvement over DT |
| **SVM + GloVe + GridSearchCV** | **Best — +15% accuracy over baseline** |
| LSTM | Deep learning baseline for sequential context |

**Key optimization:** GloVe word embeddings combined with GridSearchCV hyperparameter tuning on the SVM produced the strongest text-only classification performance, capturing semantic relationships that bag-of-words approaches miss.

### Audio Modality

| Feature Type | Models Applied |
|---|---|
| MFCCs (Mel-frequency cepstral coefficients) | SVM, Neural Network |
| Pitch | SVM, Neural Network |

Evaluated using accuracy and confusion matrices across emotion categories.

---

## Competition Context

**SemEval 2024 Task 3** is an international NLP shared task focused on *Multimodal Emotion Cause Analysis in Conversations (MECAC)* — going beyond simple emotion classification to identify what causes a specific emotional response within a dialogue.

- **Task:** Given a conversation, identify (1) the emotion of each utterance and (2) the utterance(s) that caused that emotion
- **Modalities:** Text, audio (and optionally video)
- **Emotion categories:** Joy, sadness, anger, fear, surprise, disgust, neutral
- **Challenge:** Real conversational data with contextual dependencies across turns

---

## Methodology

### Pipeline Overview

```
Raw Conversation Data (text + audio)
            │
     ┌──────┴──────┐
     ▼             ▼
Text Pipeline    Audio Pipeline
     │             │
Tokenization    MFCC Extraction
Lemmatization   Pitch Features
Stop word removal    │
     │           SVM / NN
GloVe Embeddings     │
     │             ▼
SVM / LSTM /    Emotion Predictions
Random Forest
     │
     ▼
Comparative Analysis
```

### Text Analysis (`text_analysis.ipynb`)

**Preprocessing:**
- Tokenization and lemmatization
- Stop word removal
- GloVe word embedding representation

**Models evaluated:**
- Naive Bayes — probabilistic baseline
- Decision Tree — interpretable feature splits
- Random Forest — ensemble generalization
- SVM — best performer with GloVe features
- LSTM — sequential context modeling

**Evaluation:** F1 scores per emotion class + weighted average F1

**Key finding:** SVM with GloVe embeddings + GridSearchCV hyperparameter tuning outperformed all other text models, improving accuracy by **15% over the logistic regression baseline**.

### Audio Analysis (`audio_analysis.ipynb`)

**Feature extraction:**
- **MFCCs** — captures timbral and spectral properties of speech that correlate with emotional state
- **Pitch** — prosodic feature reflecting emotional arousal

**Models evaluated:** SVM, feedforward neural network  
**Evaluation:** Accuracy, confusion matrix per emotion class

### Baseline (`base_model.ipynb`)

Logistic regression on raw text features — establishes the performance floor against which all advanced models are benchmarked. Includes essential preprocessing steps and data visualizations for dataset exploration.

---

## Getting Started

### Prerequisites

```bash
pip install pandas numpy scikit-learn tensorflow nltk gensim matplotlib seaborn
```

Download GloVe embeddings (used for text representation):
```bash
# GloVe 6B 100d embeddings
wget http://nlp.stanford.edu/data/glove.6B.zip
unzip glove.6B.zip
```

### Run the notebooks

```bash
# Clone the repository
git clone https://github.com/SaliElloh/multimodal-sentiment-analysis
cd multimodal-sentiment-analysis
```

Run notebooks in this order:

| Notebook | Description |
|---|---|
| `base_model.ipynb` | Logistic regression baseline — start here |
| `text_analysis.ipynb` | Full NLP pipeline: SVM, RF, LSTM, GloVe |
| `audio_analysis.ipynb` | Audio feature extraction + classification |

> **Note:** SemEval 2024 Task 3 dataset access requires registration at the [official task page](https://nustm.github.io/SemEval-2024-ECAC/).

---

## Key Findings

- **GloVe embeddings are critical** — switching from bag-of-words to GloVe representations drove the largest single accuracy gain across all text models
- **SVM outperforms LSTM on this dataset** — likely due to the relatively small training size; deep learning benefits require more data
- **Audio features alone are insufficient** — MFCCs and pitch provide complementary but weaker signal compared to text for this task
- **Multimodal fusion is the path forward** — combining text + audio predictions provides richer signal than either modality alone

---

## Future Work

- Integrate video/visual modality for full trimodal analysis
- Fine-tune transformer-based models (RoBERTa, BERT) on the emotion cause subtask
- Implement late fusion and attention-based fusion of text + audio embeddings
- Extend to causal span identification (not just emotion label classification)

---

## Contributors

| Name | Contributions |
|---|---|
| **Sali El-loh** | NLP pipeline, GloVe integration, SVM optimization, comparative analysis, documentation |
| **Anika Raisa-Chowdhury** | Model evaluation, data analysis |
| **Tanvi Shah** | Feature engineering, model development |
| **Seoyoung Kim** | Audio pipeline, preprocessing |
| **Dawson Kinsman** | Data processing, presentation |

---

## Author

**Sali El-loh**  
M.S. Artificial Intelligence | University of Michigan — Dearborn  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/salielloh12/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/SaliElloh)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:selloh@umich.edu)

---

## License

No license specified. Contact the author for usage permissions.


