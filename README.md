# 📝 NLP Model for Sentiment Analysis

This repository contains a Natural Language Processing (NLP) project developed as part of a course. The goal was to train a model capable of detecting **negative reviews** from a set of customer opinions.

## 📋 Instructions to run the notebook
Refer to instruccions in [Download_dataset.txt](./NLP/Dataset/Download_dataset.txt) and follow instructions to get the Dataset
To simplify the execution of the notebook, it is recommended to make a copy in your google drive and execcute it from there.

## 📌 Project Overview

- **Objective**: Classify customer reviews as negative or not.
- **Challenge**: The dataset had **imbalanced classes**, with fewer negative reviews than positive ones.
- **Approach**: Compare the performance of different models and preprocessing techniques against this imbalance.

## ⚙️ Methods and Tools

- Models used: `Logistic Regression`, `Random Forest`
- Applied techniques:
  - Use of the `class_weight='balanced'` parameter to address class imbalance
  - Removal of standard stop words (while keeping negations like _not_, _no_, _didn't_)
  - Model evaluation focused on detecting **negative reviews**

## 📊 Key Conclusions

- ✅ **Handling imbalance**:  
  Using the `class_weight='balanced'` option within models is more effective than manually applying sampling techniques.

- 🧹 **Stop words**:  
  Removing custom stop words (like _not_, _no_, _didn't_) **did not improve** results. Only standard stop words were removed.

- ⚖️ **Model performance**:  
  There's no perfect solution. The choice depends on the problem's objective: minimizing **false negatives** or **false positives** according to the context.

- 🔍 **Logistic Regression vs. Random Forest**:  
  After training both models with the complete and imbalanced dataset using `class_weight='balanced'`:
  - **Logistic Regression** performed better at detecting **negative reviews**
  - This makes it an interesting option for companies wanting to identify negative opinions and take action accordingly.

## 🔮 Future Improvements

- 🛠️ Apply **GridSearchCV** to optimize Random Forest hyperparameters.
- 🤖 Explore **Deep Learning** approaches, such as **BERT** or other transformer-based models, to capture more complex language patterns.

