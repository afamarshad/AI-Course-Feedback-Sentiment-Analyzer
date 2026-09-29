# 🎓 Course Feedback Sentiment Analysis

A multilingual AI-powered web application built with **Python and Streamlit** for analyzing student course feedback using Natural Language Processing (NLP), Machine Learning, Transformer models, and Explainable AI.

The application classifies feedback into **Positive, Neutral, or Negative** sentiment and provides additional course-wise, aspect-based, and explainable analysis.

---

## 📌 Project Overview

Educational platforms and instructors can receive a large amount of student feedback, making it difficult to manually review every response.

This project provides an interactive dashboard that processes course feedback and extracts useful insights from student reviews.

The application supports:

- Single feedback analysis
- CSV-based batch analysis
- Multilingual feedback
- Course-wise sentiment analysis
- Aspect-based sentiment analysis
- Model confidence
- Explainable AI using SHAP
- Downloadable analysis results

The project combines traditional machine learning with a multilingual Transformer model to analyze feedback written in different languages.

---

## ✨ Features

### 📝 Single Review Analysis

Enter an individual course review and receive:

- Predicted sentiment
- Model confidence
- Sentiment probabilities
- Analysis from the selected AI model

Supported sentiment categories:

- 🟢 Positive
- 🟡 Neutral
- 🔴 Negative

---

### 📂 CSV File Analysis

Upload a CSV file containing course feedback and analyze multiple reviews at once.

The application can process feedback associated with different courses and generate overall and course-wise insights.

Example CSV structure:

| Course Name | Feedback |
|---|---|
| Python for Data Science | The lessons were clear and very useful. |
| UI UX Design Essentials | The final project instructions were difficult to understand. |
| Digital Marketing Fundamentals | The course content was useful but needed more examples. |

---

### 🌍 Multilingual Sentiment Analysis

The application is designed to process feedback in multiple languages, including:

- English
- Urdu
- Chinese
- Korean
- Russian
- Spanish
- French
- German

Example:

```text
English:
The course was very useful and easy to understand.

Urdu:
یہ کورس بہت مفید ہے اور سمجھنے میں آسان ہے۔

Chinese:
这个课程非常有帮助，内容也很容易理解。

Korean:
이 과정은 매우 유익하고 이해하기 쉬웠습니다.

Russian:
Курс был очень полезным и понятным.
