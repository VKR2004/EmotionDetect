# 🎭 Emotion Classification - Text Sentiment Analysis

A machine learning project that classifies text data into six different emotion categories using Natural Language Processing (NLP) and ensemble learning techniques.

## 📋 Project Overview

This project demonstrates end-to-end text classification using Python, from data preprocessing to model evaluation. It compares two machine learning algorithms and showcases how proper NLP techniques significantly improve classification accuracy.

**Dataset:** 16,000 labeled text samples across 6 emotion categories
- **Label 0:** Sadness
- **Label 1:** Anger  
- **Label 2:** Fear
- **Label 3:** Joy
- **Label 4:** Surprise
- **Label 5:** Disgust

## 🎯 Key Results

| Model | Accuracy | F1-Score | Key Finding |
|-------|----------|----------|------------|
| Gaussian Naive Bayes | 34.9% | 0.32 | Baseline model |
| **Random Forest** | **88.0%** | **0.88** | ✅ Best performer |

The Random Forest classifier achieved **88% accuracy**, demonstrating the importance of ensemble methods for text classification tasks.

## 📊 Model Performance

### Random Forest Classification Report:
```
Emotion    Precision  Recall  F1-Score  Support
0          0.91      0.92    0.92      905
1          0.87      0.92    0.89      1053
2          0.85      0.76    0.81      271
3          0.87      0.85    0.86      459
4          0.89      0.83    0.86      397
5          0.79      0.73    0.76      115
Overall    0.88      0.88    0.88      3200
```

## 🛠️ Technology Stack

- **Python 3.11.4**
- **Data Processing:** pandas
- **NLP:** NLTK, TextBlob
- **ML Models:** scikit-learn (Gaussian Naive Bayes, Random Forest)
- **Visualization:** seaborn, matplotlib

## 📝 Data Processing Pipeline

1. **Data Loading:** Import emotion dataset (16,000 samples)
2. **Text Normalization:** Convert to lowercase
3. **Stopword Removal:** Remove common English stopwords using NLTK
4. **Lemmatization:** Reduce words to base form using TextBlob
5. **Feature Extraction:** TF-IDF vectorization
6. **Train-Test Split:** 80-20 split with random_state=0

## 🚀 Model Comparison

### Naive Bayes (Baseline)
- Simple probabilistic classifier
- Accuracy: 34.9%
- Good baseline but struggles with complex patterns

### Random Forest (Winner) ⭐
- Ensemble of decision trees
- Accuracy: 88.0%
- Better captures non-linear relationships in text

## 📈 How to Use

### Prerequisites
```bash
pip install pandas nltk textblob scikit-learn seaborn matplotlib
```

### Download Required NLTK Data
```python
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
```

### Run the Notebook
1. Update the CSV file path in the first cell to your `emotion.csv` location
2. Run all cells in order
3. View confusion matrices and classification reports

## 💡 Key Learnings

1. **Feature Engineering Matters:** Proper text preprocessing improved accuracy from 35% to 88%
2. **Algorithm Selection:** Ensemble methods outperform simple probabilistic models for text
3. **Class Balance:** Dataset shows some imbalance (Label 1: 5,362 vs Label 5: 572 samples)
4. **Validation:** Confusion matrix reveals which emotions are commonly confused with others

## 🔍 Potential Improvements

- [ ] Implement hyperparameter tuning (GridSearchCV)
- [ ] Test deep learning models (LSTM, BERT)
- [ ] Handle class imbalance with SMOTE or weighted classifiers
- [ ] Add cross-validation for more robust evaluation
- [ ] Implement model persistence (pickle/joblib)
- [ ] Create a prediction API with Flask/FastAPI
- [ ] Add unit tests

## 📁 Project Structure

```
ER3-17-02-2025-/
├── ER3.ipynb          # Main notebook with full pipeline
├── emotion.csv        # Dataset (16,000 samples)
└── README.md          # This file
```

## 🎓 Learning Outcomes

This project demonstrates:
- ✅ Complete ML pipeline implementation
- ✅ Text preprocessing and NLP techniques
- ✅ Model comparison and evaluation
- ✅ Data visualization and reporting
- ✅ Confusion matrix interpretation

## 📚 References

- [NLTK Documentation](https://www.nltk.org/)
- [scikit-learn Text Classification](https://scikit-learn.org/stable/modules/feature_extraction.html#text-feature-extraction)
- [TextBlob Documentation](https://textblob.readthedocs.io/)

## 📄 License

This project is open source and available under the MIT License.

---

**Author:** VKR2004  
**Last Updated:** May 5, 2026  
**Status:** ✅ Complete
