# Audio & Lyrics Analysis

This project explores how audio features and lyrical sentiment relate to a song’s success. Using a dataset of songs with detailed Spotify audio metrics and lyrics sentiment scores, the goal was to predict whether a song would become a hit based on its mood and composition.

I did this project while in school at the College of Charleston. However, it is still a work in progress, and I have additional avenues I would like to explore.

---

## Workflow

1. **Exploratory Data Analysis (EDA):**
   - Visualized feature distributions, correlations, and sentiment alignment.
   - Checked for outliers and feature skewness.
2. **Feature Engineering:**  
   - Combined audio and sentiment features for final modeling.
   - Extracted VADER and TextBlob sentiment from lyrics to quantify emotional and linguistic tone.
   - Performed one-hot encoding on categorical columns
3. **Model Training:**  
   - Split data into 80/20 stratified train-test sets.  
   - Compared three approaches:
     - Random Forest + balanced class weight
     - Random Forest + SMOTE
     - XGBoost
4. **Evaluation Metrics:**  
   - ROC AUC, Precision, Recall, F1-score, and Accuracy.

---

## Results

| Model | ROC AUC | Precision | Recall | F1-score |
|--------|----------|------------|----------|-----------|
| **Class-Balanced RF** | **0.947** | **0.95** | **0.79** | **0.86** |
| SMOTE RF | 0.955 | 0.80 | 0.78 | 0.79 |
| XGBoost | 0.927 | 0.72 | 0.80 | 0.76 |

**Best Model:** Class-Balanced Random Forest  
- Achieved the strongest F1 and best balance between recall and precision.  
- Demonstrated robust performance on the naturally imbalanced dataset (≈4% hits).  
- ROC AUC = **0.954**, Accuracy = **0.99** on test set.

---

## Datasets
1. [**Spotify Audio Features**](https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db/data)
3. [**Song Lyrics**](https://www.kaggle.com/datasets/carlosgdcj/genius-song-lyrics-with-language-information)

---

**William Branch**, Master’s in Data Science and Analytics — College of Charleston  
[LinkedIn](https://www.linkedin.com/in/williambranch) | [GitHub](https://github.com/williambranch)
