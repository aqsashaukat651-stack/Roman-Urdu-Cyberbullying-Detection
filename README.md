# Roman Urdu Cyberbullying Detection

## Project Overview

Roman Urdu Cyberbullying Detection is a Machine Learning project that identifies abusive and non-abusive comments written in Roman Urdu.

The project uses Natural Language Processing (NLP) techniques and a Linear Support Vector Classifier (LinearSVC) to classify comments.

## Objectives

- Detect abusive comments in Roman Urdu.
- Classify comments into Abusive and Non-Abusive categories.
- Apply text preprocessing and feature extraction.
- Evaluate machine learning performance.

## Dataset

**Dataset:** Roman Urdu Abusive Comment Dataset (5,164 comments)

**Source:** Kaggle

The dataset contains two main columns:

- `Comments`: Roman Urdu text.
- `Classes`: Comment labels.
  - `A`: Abusive
  - `NA`: Non-Abusive

After preprocessing, duplicate removal, and conflict handling, the final dataset contains 4,892 comments.

## Technologies Used

- Python
- Pandas
- Regular Expressions
- Scikit-learn
- TF-IDF Vectorizer
- LinearSVC
- Kaggle Notebooks

## Machine Learning Workflow

1. Load the dataset.
2. Clean and normalize class labels.
3. Remove duplicate comments.
4. Preprocess Roman Urdu text.
5. Remove conflicting labels and duplicate cleaned comments.
6. Split the dataset into training and testing sets (80/20).
7. Extract character-level TF-IDF features.
8. Train the LinearSVC classifier.
9. Evaluate model performance.

## Model Configuration

- Feature extraction: TfidfVectorizer
- Analyzer: `char_wb`
- Maximum features: 10,000
- N-gram range: (2, 4)
- Classification algorithm: LinearSVC
- Class balancing: Enabled
- Maximum iterations: 2,000

## Results

**Final Model Accuracy: 83.35%**

| Metric | Abusive (A) | Non-Abusive (NA) |
|---|---:|---:|
| Precision | 0.83 | 0.84 |
| Recall | 0.81 | 0.86 |
| F1-score | 0.82 | 0.85 |

## Model Testing

Example:

**Input:** Tum bilkul jahil ho

**Prediction:** Abusive (A)

## Limitations

- Designed specifically for Roman Urdu comments.
- May not correctly understand sarcasm, context, or spelling variations.
- Predictions are not guaranteed to be correct.
- The model is a text-classification prototype and should not be treated as a complete cyberbullying moderation system.

## Future Improvements

- Increase dataset size and diversity.
- Improve detection of spelling variations.
- Test additional machine learning algorithms.
- Develop a simple web interface.
- Improve detection of context-dependent abusive language.

## Author

Developed as a Machine Learning / Data Science academic project.

## License

This project is intended for educational and research purposes.
