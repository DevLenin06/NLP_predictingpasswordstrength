# Predicting Password Strength Model

This respository stores a machine learning model that is built to predict the strength of passwords based on different features of each password itself. I accomplished this with the application of  Natural Lnaguage Processing(NLP) Techniques. This model uses Logistic Regression and was trained using a data containing a variety of passwords and their corresponding strength ratings.  

## Overview
The goal of this project is to predict the strength of passwords and classify them into three main categories:
- `0`: Weak
- `1`: Medium
- `2`: Strong

This model preprocesses the password data and extracts features such as length, frequency of lowercase/uppercase characters, digits, and special characters. It also applies Natural Language Processing (NLP) techniques, such as TF-IDF vectorization, to convert password strings into numerical feature vectors FInally it applies a machine learning model (Logistic Regression) to predict password strength.

## Data Description
The dataset used contains the following columns:
- `password`: The actual password string.
- `strength`: The strength of the password (0: Weak, 1: Medium, 2: Strong).
- `length`: Length of the password.
- `lowercase_freq`: Frequency of lowercase characters in the password.
- `uppercase_freq`: Frequency of uppercase characters in the password.
- `digit_freq`: Frequency of digits in the password.
- `special_char_freq`: Frequency of special characters in the password.

## Libraries
The folllowing Python libraries are required to run this project
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn`
- `scipy`

You can install them using the following command
``` bash
pip install -r requirements.txt
```

## Model Training

The model is trained using the following steps:

1. Data Preprocessing:
   - The passwords are turned into feature vectors using `TfidfVectorizer`.
   - Additional password statistics (length, frequency of lowercase, uppercase, digits, and special characters) are appended to the feature matrix.
2. Model:
   - The Model is a Multinomial Logistic Regression classifier, that is trained to predict the strength of a password based on extracted features.
3. Training:
   - The data is split into training and testing sets (80% training, 20% testing)

## Model Evaluation
After training the model, predictions are made on the test set, and the following evaluation is done:
- Confusion Matrix to understand the model's performance in classifying the password strength.
- Classification Report to display metrics like precision, recall, and F1-score.

The predictions are shown as a counter for the number of occurences of each strength category in the predicted labels. 

   

