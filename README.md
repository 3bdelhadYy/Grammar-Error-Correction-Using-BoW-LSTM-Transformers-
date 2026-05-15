# Grammar Error Correction using Deep Learning

This project implements and compares multiple deep learning architectures for the Grammar Error Correction (GEC) task using a large-scale subset of the C4 dataset.

## Models Implemented

- Bag-of-Words Feedforward Neural Network (BoW-FNN)
- LSTM Seq2Seq
- LSTM Seq2Seq with Bahdanau Attention
- Transformer Encoder-Decoder

---

# Dataset

The dataset was built from the C4 (Colossal Clean Crawled Corpus) dataset.

- 100,000 samples were selected from each of 10 files
- Total dataset size: ~1,000,000 sentence pairs
- Data was shuffled and cleaned before training

Each sample contains:
- Incorrect input sentence
- Corrected target sentence

---

# Preprocessing

The preprocessing pipeline includes:

- Text cleaning
- Lowercasing
- Tokenization
- Vocabulary construction
- Sequence vectorization
- Special start/end tokens

Vocabulary Size:
- 10,000 tokens

Maximum Sequence Length:
- 100 tokens

---

# Evaluation Metrics

The models were evaluated using:

- Token-Level Accuracy
- Precision
- Recall
- F0.5 Score

F0.5 is commonly used in GEC tasks because it prioritizes precision over recall.

---

# Results

| Model | Accuracy | Precision | Recall | F0.5 |
|---|---|---|---|---|
| BoW-FNN | 0.0350 | 0.0495 | 0.0682 | 0.0523 |
| LSTM Seq2Seq | 0.1098 | 0.3364 | 0.3302 | 0.3351 |
| LSTM + Attention | 0.1632 | 0.4543 | 0.4354 | 0.4504 |
| Transformer | 0.2116 | 0.5612 | 0.5245 | 0.5535 |

The Transformer model achieved the best overall performance.

---

# Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

# Features

- Large-scale NLP training pipeline
- Custom inference pipelines
- Attention mechanism implementation
- Transformer architecture
- Memory-safe preprocessing
- Comparative model analysis

---

# Future Improvements

- Beam search decoding
- Pretrained Transformer models
- Larger vocabulary sizes
- Better dataset filtering
- Multilingual GEC support

---

# Author

Abdelhady Mostafa
