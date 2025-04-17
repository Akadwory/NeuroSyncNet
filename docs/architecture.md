# NeuroSyncNet Architecture Overview

## Pipeline

1. **EEG Preprocessing**
   - Bandpass filtering (8–30Hz)
   - ICA/EOG artifact rejection
   - Epoch slicing (0–0.3s window)

2. **Data Loader + Augmentation**
   - Torch dataset with real-time slicing
   - Time masking, jitter, and patch embedding

3. **Encoder**
   - Patch Embedding Layer (per channel or across time)
   - Positional Encoding

4. **Causal Transformer**
   - Masked self-attention (only attends to past)
   - Multi-head attention + FFN stack

5. **Latent Forecasting**
   - Predict future EEG embeddings or target class

6. **Classifier Head**
   - Fully connected layers → 4-class softmax

7. **Interpretability**
   - Attention weight visualization
   - EEG heatmaps over time

---

## Loss Functions
- Cross-Entropy (classification)
- MSE / Cosine Similarity (forecast latent embeddings)
- Contrastive Triplet Loss (optional for pretraining)
