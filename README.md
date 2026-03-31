# Zomato Restaurant Analysis and Sentiment Classification

## Project Overview

This project performs end-to-end data analysis and machine learning on Zomato restaurant data. It combines Exploratory Data Analysis (EDA) with Natural Language Processing (NLP) to extract insights from restaurant metadata and customer reviews, and builds predictive models to classify review sentiment.

The workflow includes data preprocessing, visualization, feature engineering, model comparison, and deployment-ready inference.

---

## Objectives

- Analyze restaurant data to identify patterns in ratings, cost, and cuisines  
- Understand customer behavior through review analysis  
- Perform sentiment classification on textual reviews  
- Compare multiple machine learning models and select the best-performing one  
- Simulate real-world deployment by saving and loading the trained model  

---

## Dataset Description

The project uses two datasets:

### 1. Restaurant Metadata
- Restaurant Name  
- Location  
- Cuisines  
- Cost for two  
- Rating  

### 2. Customer Reviews
- Restaurant Name (used for merging)  
- Review Text  
- Rating  

Both datasets are merged using:

Restaurant (reviews) ↔ Name (restaurants)

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Pickle  

---

## Project Workflow

### 1. Data Understanding
- Dataset inspection using .info() and .shape()  
- Feature identification  
- Missing value analysis  

### 2. Data Cleaning and Preprocessing
- Handling missing values based on feature importance  
- Removing duplicates  
- Text cleaning (lowercasing, removing special characters)  
- Feature standardization  
- Sentiment label creation from ratings  

### 3. Exploratory Data Analysis (EDA)

A total of 15 visualizations were created:

Univariate Analysis:
- Rating distribution  
- Sentiment distribution  
- Cost distribution  
- Top cuisines  
- Review length  

Bivariate Analysis:
- Rating vs Cost  
- Sentiment vs Rating  
- Cost vs Sentiment  
- Cuisine vs Rating  

Multivariate Analysis:
- Correlation heatmap  
- Pairplot  
- Multi-variable scatter plots  

### 4. Feature Engineering

- Text data transformed using TF-IDF Vectorization  
- Top 5000 features selected based on importance  

### 5. Model Building

Multiple models were trained and evaluated:
- Logistic Regression  
- Naive Bayes  
- Random Forest  

### 6. Model Evaluation

- Accuracy Score  
- Classification Report  
- Confusion Matrix  
- Model comparison using visualization  

### 7. Model Selection

- Best model selected based on performance metrics  
- Naive Bayes typically performs well for text classification  

### 8. Model Saving and Loading

- Best model saved using pickle  
- TF-IDF vectorizer saved separately  
- Model reloaded and tested on new sample inputs  

---

## Key Insights

- Ratings are generally skewed toward higher values  
- Positive sentiment dominates the dataset  
- Cost does not strongly influence ratings  
- Certain cuisines consistently receive higher ratings  
- Customer reviews are mostly short but informative  

---

## Machine Learning Outcome

- Successfully built a sentiment classification model  
- Demonstrated effective use of NLP techniques  
- Achieved reliable performance across multiple models  
- Simulated deployment through model persistence and inference  

---

## Future Improvements

- Use advanced NLP models such as LSTM or BERT  
- Implement a recommendation system  
- Deploy as a web application using Streamlit  
- Integrate real-time API for predictions  
- Apply clustering for unsupervised insights  

---

## Project Structure

zomato-project/
│
├── models/
│   └── (saved model files such as best_sentiment_model.pkl, tfidf_vectorizer.pkl)
│
├── .gitignore
├── README.md
├── Zomato_Project.ipynb

---

## How to Run

Install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn

Run the notebook:

jupyter notebook

---

## Conclusion

This project demonstrates how combining structured restaurant data with unstructured review text can generate meaningful insights and build effective predictive models. It highlights the practical application of EDA, NLP, and machine learning in solving real-world problems.
