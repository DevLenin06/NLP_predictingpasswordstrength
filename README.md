# Predicting Password Strength Model

This respository stores a machine learning model that is built to predict the strength of passwords based on different features of each password itself. I accomplished this with the application of  Natural Lnaguage Processing(NLP) Techniques. This model uses Logistic Regression and was trained using a data containing a variety of passwords and their corresponding strength ratings.  

## Overview
The goal of this project is to predict the strength of passwords and classify them into three main categories:
- `0`: Weak
- `1`: Medium
- `2`: Strong

This model preprocesses the password data and extracts features such as length, frequency of lowercase/uppercase characters, digits, and special characters. It also applies Natural Language Processing (NLP) techniques, such as TF-IDF vectorization, to convert password strings into numerical feature vectors FInally it applies a machine learning model (Logistic Regression) to predict password strength.
