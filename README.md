# Multimodal Explainable AI for Diabetes Readmission Prediction

A multimodal AI system combining structured EHR features with 
LLM-generated synthetic clinical text for 30-day diabetes 
readmission prediction.

## Results

| Model | AUC-ROC | F1 |
|---|---|---|
| Late Fusion NN | **0.9067** | 0.6182 |
| Early Fusion NN | 0.8649 | 0.5271 |
| XGBoost | 0.6781 | 0.0310 |
| Tabular-Only NN | 0.6136 | 0.2352 |
| **Text modality gain** | **+0.2513** | **+0.2919** |

## Pipeline

- **Phase 1:** Data preprocessing (Diabetes 130-US Hospitals, UCI)
- **Phase 2:** Synthetic note generation (LLaMA-3.1-8B) + 
  Bio+ClinicalBERT embeddings
- **Phase 3:** Model training — LR, RF, XGBoost, Tab-NN, 
  Early Fusion NN, Late Fusion NN
- **Phase 4:** SHAP explainability + LLM clinical recommendations
- **Phase 5:** Publication-ready figures and tables

## Requirements

- Python 3.10+
- Google Colab (recommended, GPU runtime)
- Groq API key (free tier)

## Setup

1. Open `Multimodal_System_ML_Research.ipynb` in Google Colab
2. Add Groq API key to Colab Secrets as `GROQ_API_key`
3. Mount Google Drive
4. Run cells sequentially

## Dataset

Diabetes 130-US Hospitals for Years 1999–2008  
UCI ML Repository, ID 296, CC BY 4.0  
Auto-downloaded via `ucimlrepo`

## Paper

Submitted to Informatics in Medicine Unlocked (Elsevier)

## Authors

- Aiman Sadiev — Ala-Too International University, Kyrgyzstan
