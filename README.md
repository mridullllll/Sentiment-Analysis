# Sentiment-Analysis

## Introduction
This project focuses on analyzing and predicting the sentiment of reviews. Using a dataset of reviews from various sources, we aim to clean, process, and extract insights from the text data. We also implement different machine learning models to classify the reviews and predict their sentiment.

## Technical Stack
- **Programming Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, NLTK, Afinn

## Dataset
The dataset comprises reviews collected from multiple sources, including Trip Advisor, Google, and Facebook. The data includes review text, review ratings, and the source of the reviews. The dataset is used to understand patterns and sentiments in the reviews.

## Pre-processing
The pre-processing steps involved:
- Identifying and keeping the first occurrence of duplicate reviews by the same person on the same day.
- Keeping the first occurrence of reviews by the same person within a 7-day interval.
- Implementing standard text pre-processing techniques: 
  - Contraction replacement
  - Stop words removal
  - Number and symbols removal
  - Lowercasing
  - Slang correction
  - Spell correction
  - Translation to English
  - Stemming and lemmatization

## Modeling
Several models and techniques were used to analyze and predict sentiments:
- **Exploratory Data Analysis (EDA):** Visualized review ratings and sources.
- **Supervised Learning:**
  - Multinomial Naive Bayes classifier was used for sentiment prediction using TF-IDF features.
  - Handled class imbalance using Random Over Sampling.
- **Unsupervised Learning:**
  - Afinn Lexicon was used for sentiment prediction, providing sentiment scores for each review.

## Results
The analysis revealed that:
- The most common review rating is 5, indicating positive feedback.
- "Trip Advisor" has the highest number of reviews among the sources.
- The Multinomial Naive Bayes model achieved high validation and test accuracies (87% and 88.3% respectively) using TF-IDF features.
- After over-sampling, the model's validation and test accuracies slightly decreased to 80% and 80.5% respectively.
- Afinn Lexicon provided sentiment scores ranging from -15 to 49, effectively identifying the polarity of sentiments in the review texts.

## Analysis & Insights
- The Multinomial Naive Bayes classifier performed well, indicating strong correlation between specific terms in the reviews and their classified sentiments.
- The model generalizes well to unseen data, suggesting robustness in prediction.
- Afinn Lexicon offers a straightforward approach to sentiment analysis without the need for complex models.

## Challenges & Considerations
- Handling imbalanced data was a significant challenge, addressed by Random Over Sampling.
- Some classes had very few samples, limiting the applicability of under-sampling or SMOTE techniques.
- Future work could explore more complex models and additional data sources to further enhance prediction accuracy and insights.

## Conclusion
This project demonstrates effective techniques for text preprocessing, sentiment analysis, and prediction using both supervised and unsupervised learning methods. Future improvements could focus on refining models and expanding the dataset for more robust results.
