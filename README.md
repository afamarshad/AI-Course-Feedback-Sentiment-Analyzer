# 🎓 Course Feedback Sentiment Analysis

A multilingual AI-powered web application built with **Python and Streamlit** for analyzing student course feedback using **Natural Language Processing (NLP), Machine Learning, Transformer models, and Explainable AI**.

The application classifies student feedback into **Positive, Neutral, or Negative** sentiment and provides additional **course-wise, aspect-based, confidence, explainable, and improvement insights**.

---

## 🚀 Live Demo

Try the deployed application:

👉 **[Course Feedback Sentiment Analyzer · Streamlit](https://ai-course-feedback-sentiment-analyzer.streamlit.app/)**

---

## 📌 Project Overview

Educational platforms and instructors can receive a large amount of student feedback, making it difficult to manually review every response.

This project provides an interactive AI-powered dashboard that processes student feedback and converts unstructured reviews into meaningful insights.

The application supports both **individual review analysis** and **CSV-based batch analysis**, allowing users to identify overall sentiment patterns, course-specific trends, important feedback aspects, and areas for improvement.

The project combines a traditional machine learning model with a multilingual Transformer model to analyze feedback written in different languages.

---

## ✨ Key Features

* 📝 Single student review analysis
* 📂 CSV-based batch analysis
* 🌍 Multilingual sentiment analysis
* 📊 Overall sentiment distribution
* 🎓 Course-wise sentiment analysis
* 🔍 Aspect-based sentiment analysis
* 🧠 Explainable AI using SHAP
* 📈 Sentiment probability and confidence information
* 💡 Improvement suggestions
* 📥 Downloadable analysis results
* 📦 Course-wise downloadable analysis packages
* 📋 Detailed review-level analysis

---

## 📝 Single Review Analysis

The **Single Review Analysis** section allows users to enter an individual student review and analyze it using the available AI models.

The analysis can provide:

* Predicted sentiment
* Sentiment probability
* Model confidence
* Selected model prediction
* Aspect-based insights
* Improvement suggestions

### Sentiment Categories

The application classifies feedback into three categories:

* 🟢 **Positive**
* 🟡 **Neutral**
* 🔴 **Negative**

### Example

```text
The instructor explained every concept clearly and the course was very useful.
```

Possible result:

```text
Sentiment: Positive
```

---

## 📂 CSV File Analysis

The **CSV Analysis** section allows users to upload multiple student reviews and analyze them in a single batch.

The application can process feedback associated with different courses and generate overall and course-specific insights.

### Example CSV Structure

| Course Name                    | Feedback                                                     |
| ------------------------------ | ------------------------------------------------------------ |
| Python for Data Science        | The lessons were clear and very useful.                      |
| UI UX Design Essentials        | The final project instructions were difficult to understand. |
| Digital Marketing Fundamentals | The course content was useful but needed more examples.      |

The CSV analysis can generate:

* Overall sentiment distribution
* Course-wise sentiment distribution
* Course-wise aspect analysis
* Sentiment percentages
* Aspect-level sentiment
* Confidence information
* Detailed review-level results
* Improvement suggestions
* Downloadable analysis packages

---

## 🌍 Multilingual Sentiment Analysis

The application is designed to process student feedback written in multiple languages.

Supported languages include:

* English
* Urdu
* Chinese
* Korean
* Russian
* Spanish
* French
* German

### Example Feedback

**English**

```text
The course was very useful and easy to understand.
```

**Urdu**

```text
یہ کورس بہت مفید ہے اور سمجھنے میں آسان ہے۔
```

**Chinese**

```text
这个课程非常有帮助，内容也很容易理解。
```

**Korean**

```text
이 과정은 매우 유익하고 이해하기 쉬웠습니다.
```

**Russian**

```text
Курс был очень полезным и понятным.
```

The multilingual functionality is primarily supported through the fine-tuned multilingual Transformer model.

---

## 🤖 Machine Learning Models

The project uses multiple approaches for sentiment classification.

### 1. TF-IDF + Logistic Regression

The first approach is a traditional machine learning pipeline using:

* **TF-IDF (Term Frequency–Inverse Document Frequency)**
* **Logistic Regression**
* Sentiment probability estimation

This model provides a lightweight baseline for sentiment classification.

The trained model files are:

```text
coursera_tfidf_logistic_model.pkl
coursera_tfidf_vectorizer.pkl
```

---

### 2. Multilingual DistilBERT

The project also uses a fine-tuned multilingual **DistilBERT** Transformer model.

The model is designed to process multilingual course feedback and classify it into three sentiment categories:

```text
0 → Negative
1 → Neutral
2 → Positive
```

The trained Transformer model is hosted on **Hugging Face** rather than storing large model files directly in the GitHub repository.

This approach helps avoid GitHub file-size limitations and makes deployment on Streamlit Community Cloud more practical.

---

## 🔄 Combined Model Analysis

The application can also use a **Combined** approach that incorporates probability outputs from the available sentiment models.

The purpose of combining model outputs is to use information from both the traditional machine learning model and the Transformer-based model when generating sentiment predictions.

The application allows users to select the available analysis approach according to the functionality provided in the interface.

---

## 🔍 Aspect-Based Sentiment Analysis

Overall sentiment alone does not always explain what students liked or disliked about a course.

The application therefore performs **aspect-based analysis** using predefined course-related aspects.

Current aspects include:

* **Course Content**
* **Instructor**
* **Assignments**
* **Difficulty**
* **Learning Experience**
* **Structure**
* **Platform**
* **Certificates**
* **Duration**
* **Value**

### Example

```text
The instructor was excellent, but the assignments were too difficult.
```

The feedback may be interpreted at the aspect level as:

```text
Instructor → Positive
Assignments → Negative
```

This provides more detailed information than a single overall sentiment label.

---

## 🎓 Course-Wise Analysis

When multiple courses are included in the uploaded CSV file, the application can organize the feedback according to course.

Course-wise analysis can provide:

* Total reviews
* Positive reviews
* Neutral reviews
* Negative reviews
* Sentiment percentages
* Aspect distribution
* Aspect-level sentiment
* Course-specific insights
* Improvement suggestions

This allows instructors or course administrators to identify patterns within individual courses.

---

## 📊 Data Visualization

The application provides visual summaries to make large amounts of feedback easier to understand.

Visual analysis can include:

* Overall sentiment distribution
* Course-wise sentiment distribution
* Aspect-based sentiment insights
* Sentiment percentages
* Course-level comparisons
* Review analysis

The visualizations help convert large collections of student comments into more understandable patterns.

---

## 🧠 Explainable AI with SHAP

The application includes an **Explainable AI (XAI)** section using **SHAP (SHapley Additive exPlanations)**.

SHAP can help explain which input features contributed to a model's prediction.

For text classification, this can provide additional insight into why certain words or features contributed toward a particular sentiment.

The purpose of the Explainable AI component is to make the model's predictions more transparent rather than presenting only the final sentiment label.

---

## 📈 Sentiment Probability and Confidence

Along with the predicted sentiment, the application can provide probability and confidence information associated with the prediction.

For example:

```text
Prediction: Positive
Confidence: 94.2%
```

Confidence represents the model's level of confidence in its prediction and should not be interpreted as a guarantee that the prediction is correct.

---

## 💡 Improvement Suggestions

The application can generate improvement suggestions based on the sentiment and aspects identified in student feedback.

For example, repeated negative feedback related to:

```text
Assignments
Difficulty
Course Content
```

can be used to identify areas that may require attention.

For batch analysis, the application can also provide overall aspect-based suggestions based on the analyzed feedback.

These insights can help instructors and course designers identify potential areas for improvement.

---

## 📥 Downloadable Results

The application provides downloadable results from the analysis.

Depending on the analysis performed, users can download information such as:

* Sentiment results
* Course-wise analysis
* Aspect analysis
* Confidence information
* Detailed review results
* Improvement suggestions
* Course-wise analysis packages

This allows the generated insights to be saved and reviewed outside the Streamlit application.

---

## 🖥️ Application Sections

The current application includes the following main sections:

### 📝 Single Review Analysis

Analyze an individual student review and receive sentiment, probability, confidence, aspect, and improvement insights.

### 📊 CSV Analysis

Upload and analyze multiple student reviews and generate overall and course-wise results.

### 🔍 Aspect Analysis

Explore sentiment associated with predefined course-related aspects.

### 🧠 Explainable AI (SHAP)

Explore model explanations and feature-level contributions to sentiment predictions.

### ℹ️ About

Provides information about the project and its purpose.

---

## 🛠️ Technology Stack

### Programming Language

* Python

### Web Application

* Streamlit

### Machine Learning

* Scikit-learn
* TF-IDF
* Logistic Regression

### Deep Learning & NLP

* Hugging Face Transformers
* Multilingual DistilBERT
* PyTorch

### Explainable AI

* SHAP

### Data Processing

* Pandas
* NumPy

### Visualization

* Matplotlib
* Streamlit visualization components

### Model Hosting

* Hugging Face

### Version Control

* GitHub

### Deployment

* Streamlit Community Cloud

---

## 📁 Project Structure

A simplified project structure is:

```text
Course-Feedback-Sentiment-Analysis/
│
├── app.py
├── requirements.txt
├── README.md
│
├── coursera_tfidf_logistic_model.pkl
├── coursera_tfidf_vectorizer.pkl
│
└── other project files/
```

The multilingual DistilBERT model is hosted on Hugging Face and loaded by the application when required.

Large Transformer model files therefore do not need to be stored directly in the GitHub repository.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Open the Project Directory

```bash
cd Course-Feedback-Sentiment-Analysis
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

### 4. Activate the Environment

On Windows:

```bash
.venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Run the Application

```bash
streamlit run app.py
```

The application will open in your default web browser.

---

## ☁️ Streamlit Community Cloud Deployment

The application can be deployed using **Streamlit Community Cloud**.

General deployment process:

1. Push the project files to GitHub.
2. Connect the GitHub repository to Streamlit Community Cloud.
3. Select the appropriate repository and branch.
4. Set `app.py` as the main application file.
5. Streamlit installs the dependencies listed in `requirements.txt`.
6. Deploy the application.
7. The application loads the required models and resources.

### Live Application

👉 **[Course Feedback Sentiment Analyzer · Streamlit](https://ai-course-feedback-sentiment-analyzer.streamlit.app/)**

---

## 📦 Project Dependencies

The project's Python dependencies are specified in:

```text
requirements.txt
```

These dependencies include the libraries required for:

* Streamlit application functionality
* Data processing
* Machine learning
* Transformer-based NLP
* Explainable AI
* Visualization

---

## ⚠️ Limitations

Machine learning predictions are not guaranteed to be correct for every piece of feedback.

Potential limitations include:

* Ambiguous feedback
* Sarcasm
* Very short reviews
* Mixed positive and negative sentiment
* Language-specific expressions
* Domain-specific terminology
* Multilingual NLP limitations
* Incorrect or uncertain aspect identification
* Model confidence not necessarily representing real-world prediction accuracy

The application should therefore be considered an **AI-assisted feedback analysis tool** rather than a replacement for human interpretation of student feedback.

---

## 🎯 Project Objective

The primary objective of this project is to demonstrate how **AI, NLP, and machine learning** can be used to transform large amounts of unstructured student feedback into structured and useful insights.

The project combines:

**Sentiment Analysis → Aspect Analysis → Course-Wise Insights → Explainable AI → Improvement Suggestions**

to provide a more comprehensive approach to educational feedback analysis.

---

## 👩‍💻 Author

**Afsah Arshad**

Certified AI Practitioner | Building Intelligent Solutions with Python, Machine Learning & Deep Learning 

This project was developed as an AI/NLP application for analyzing educational course feedback and demonstrating practical applications of:

* Machine Learning
* Natural Language Processing
* Multilingual NLP
* Transformer Models
* Explainable AI
* Educational Data Analysis

---

## ⭐ Project Demo

🚀 **Try the live application:**

👉 **[Course Feedback Sentiment Analyzer · Streamlit](https://ai-course-feedback-sentiment-analyzer.streamlit.app/)**

If you find the project useful, consider giving the repository a ⭐ on GitHub.
