# Predicting Password Strength Model

This respository stores a machine learning model that is built to predict the strength of passwords based on different features of each password itself. I accomplished this with the application of  Natural Lnaguage Processing(NLP) Techniques. This model uses Logistic Regression and was trained using data containing a variety of passwords and their corresponding strength ratings.  

## Overview
The goal of this project is to predict the strength of passwords and classify them into three main categories:
- `0`: Weak
- `1`: Normal
- `2`: Strong

This model preprocesses the password data and extracts features such as length, frequency of lowercase/uppercase characters, digits, and special characters. It also applies Natural Language Processing (NLP) techniques, such as TF-IDF vectorization, to convert password strings into numerical feature vectors FInally it applies a machine learning model (Logistic Regression) to predict password strength.

## Data Description
The dataset used contains the following columns:
- `password`: The actual password string.
- `strength`: The strength of the password (0: Weak, 1: Normal, 2: Strong).
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


## Example of Prediction: 
For a given password such as `@123abcd`, the model predicts a strength class of (0, 1, or 2).

## Usage
To use the trained model for predicting password strength:

1.Clone this repository:
Download or Clone this repository to your local machine:
``` bash
git clone https://github.com/DevLenin06/NLP_predictingpasswordstrength/tree/main
cd NLP_predictingpasswordstrength
```

2.Open Jupyter Notebook:
Ensure you have Jupyter Notebook installed. Then, open the notebook file:
``` bash
jupyter notebook NLP_predictingpasswordstrength.ipynb
```

3.Run the Notebook:
- Execute all the cells in the notebook
- The notebook will train/load the model and include a predict() function for evaluating password strengths.

4. Predict Password Strength
- Once the notebook has run sucessfully, you can call the predict function locally in a code cell by typing `predict()`. The model will then provide a prompt to enter a password and then return the strength of that password. 





   

