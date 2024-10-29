# Amazon-Review-Rating-Predction
Link to data set https://www.kaggle.com/competitions/final-competition-fall2023/overview

Library Imports and Setup:

Imports libraries including pandas, numpy, scikit-learn, and nltk.
Downloads nltk resources such as wordnet for lemmatization and stopwords for filtering English stop words.
Data Loading:

Defines file paths for training and testing datasets.
Loads data into pandas DataFrames, handling encoding and potential errors during import.
Preprocessing:

Handles missing data in 'summary' and 'text' columns by filling missing values.
Applies lemmatization to these columns to standardize words.
Combines 'summary' and 'text' into a single 'full_text' column for further analysis.
Feature Extraction:

Uses TfidfVectorizer to convert 'full_text' into a matrix of TF-IDF features, evaluating the relevance of words within documents.
Machine Learning Pipeline:

Constructs a pipeline combining TfidfVectorizer and RandomForestClassifier.
Employs GridSearchCV for hyperparameter tuning to optimize the classifier's settings.
Model Training and Evaluation:

Trains the model using the processed training data.
Evaluates model performance using accuracy scores and generates a detailed classification report.
Prediction and Output:

Preprocesses testing data using the same steps as training data.
Uses the trained model to make predictions on testing data.
Outputs predictions into a CSV file for external use or review.
Error Handling:

Includes a try-except block to catch and report errors during data loading, processing, or model execution phases.
