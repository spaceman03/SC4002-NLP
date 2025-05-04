## Sentiment Classification on MOvie Review Dataset
This repository contains the implementation of a sentence-level sentiment classification system built on top of pretrained word embeddings such as Word2Vec and GloVe. The project explores standard Natural Language Processing (NLP) techniques and deep learning architectures — including **RNN, CNN, BiLSTM, and BiGRU** — to effectively assign sentiment labels to sentences.

To further enhance model performance, we also experimented with **Ensemble** methods, combining predictions from multiple models to achieve more robust results.

## 📌 Abstract
The goal of this project is to build a general-purpose text classification system using pretrained word embeddings, with a focus on **sentiment classification**. This serves as a hands-on exercise in:
- Applying pretrained word embeddings (Word2Vec, GloVe)
- Building and training deep learning models for sentence classification
- Evaluating classifier performance on sentiment analysis tasks

## 🛠️ Features
- Pretrained Embedding Integration: Leverages pretrained Word2Vec and GloVe vectors.
- Model Architectures: Includes implementations of typical deep learning models such as:
    - Simple Feedforward Networks
    - RNN / LSTM / GRU-based models
    - CNN-based models for sentence classification
- Evaluation Metrics: Accuracy, Precision, Recall, F1-score.
- Training & Validation: Includes scripts for model training, validation, and performance tracking.

## 📑 Results
### Word2Vec: Model Accuracy (%) by OOV Handling Strategy
| Model | Cosine Similarity | BPE + Stemming | Back Off Method (sympell + stopwords) |
|:---|:---|:---| :--- |
RNN (Handle OOV) | **77.77%** | 75.89% | 65.38% |
RNN (Handle OOV with Word Embeddings Update | 77.11% | 76.36% | **79.92%** |
biLSTM | 78.33% | **79.17%** | 78.33% |
biGRU | 72.70% | 80.30% | **80.39%** |
CNN | 77.95% | 77.67% | **79.17%** |
RNN (Update Word Embeddings) | 78.70% | 79.64% | **80.95%** |
Emsemble | 81.23% | 81.14% | **82.27%** |

### GloVe: Model Accuracy (%) by OOV Handling Strategy
| Model | Cosine Similarity | BPE + Stemming | Back Off Method (sympell + stopwords) |
|:---|:---|:---| :--- |
RNN (Handle OOV) | 78.04% | 78.70% | 76.54% |
RNN (Handle OOV with Word Embeddings Update | 80.58% | 81.70% | 81.42% |
biLSTM | 80.39% | 81.14% | 82.45% |
biGRU | 81.42% | 81.14% | 81.98% |
CNN | 74.10% | 78.42% | 79.08% |
RNN (Update Word Embeddings) | 78.14% | 67.26% | 81.33% |
Emsemble | 82.00% | 82.64% | 83.39% |

## Getting Started

### Prerequisites
As the project is run using Python, please ensure that Python 3.12 is installed in your device.

### Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/spaceman03/SC4002-NLP.git
    cd SC4002_NLP
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Jupyter Notebook
1. Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

2. Open and run `SC4002_G10_Word2vec_Backoff.ipynb` within the Jupyter interface.
