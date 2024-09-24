# Multiclass Text Classification of Presidential Campaign Tweets

## Introduction

Welcome to the Big Data Challenge (BDC) Satria Data 2024 project repository! This repository showcases a sophisticated project focused on analyzing social media data from Platform X (formerly known as Twitter) during the Indonesian presidential campaign of 2024. The objective is to classify tweets into one of the eight Astagatra categories, which are key components of national resilience:

- **Ideology**: Fundamental values and principles guiding the nation.
- **Politics**: Government systems, policies, and political processes.
- **Economy**: Management of economic resources for societal prosperity.
- **Socio-Cultural**: Social values, cultural norms, and societal life.
- **Defense and Security**: National defense and internal security.
- **Natural Resources**: Management and utilization of natural resources.
- **Geography**: Physical location and environmental conditions affecting life and policy.
- **Demography**: Population structure, growth, distribution, and dynamics.

## Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Evaluation Results](#evaluation-results)
- [Tools and Technologies](#tools-and-technologies)
- [Submission](#submission)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contributing](#contributing)
- [Contributors](#contributors)

## Problem Statement

This project addresses the challenge of handling a massive volume of User Generated Content (UGC) from Platform X. The task is to develop a robust multiclass text classification model that can categorize tweets into the specified Astagatra classes, despite the complexities of unstructured data, language nuances, ambiguity, sarcasm, and typos.

## Dataset

The datasets provided for this project include:
- **[Training Dataset](https://bit.ly/dataset_bdc_2024)**: A CSV file containing tweets and their corresponding labels.
- **[Unlabeled Dataset](https://bit.ly/dataset_unlabeled_bdc_2024)**: A CSV file where the goal is to predict the correct labels.


## Methodology

Our approach to solving this problem is methodical and comprehensive:

1. **Text Cleansing**: We meticulously cleaned the text data through several steps:
   - **Removing Mentions and Patterns**: Cleared Twitter-specific elements like `@username`, `re`, and `rt`.
   - **Hashtag Preprocessing**: Processed hashtags to integrate them into the context of the tweets.
   - **Lowercasing**: Converted all text to lowercase to maintain consistency.
   - **Removing URLs**: Stripped out URLs using regular expressions.
   - **Removing Numbers**: Removed numeric characters to focus on the textual content.
   - **Removing Non-ASCII Characters**: Ensured compatibility by removing non-ASCII characters.
   - **Removing Non-Alphanumeric Characters**: Cleansed the text further by eliminating non-alphanumeric characters (excluding spaces).
   - **Trimming Excessive Whitespace**: Reduced multiple spaces to a single space for consistency.
   - **Final Cleanup**: Removed any remaining unwanted characters and underscores.
   - **Removing Stopwords**: Applied NLP techniques to filter out non-essential stopwords.
2. **Data Splitting**: Divided the dataset into training and testing sets for a thorough evaluation.
3. **Augmenting Minority Classes**: Applied data augmentation techniques to balance the minority classes in the training data.
4. **TF-IDF Vectorization**: Transformed the textual data into numerical features using TF-IDF vectorization.
5. **Model Training**: Trained multiple machine learning models, including Logistic Regression, SVM, and others.
6. **Evaluation**: Assessed the models using accuracy, balanced accuracy, and other relevant metrics.
7. **Model Selection**: Selected Logistic Regression as the best-performing model based on evaluation metrics.
8. **Inference**: Used the selected model to predict labels for the unlabeled dataset.

## Evaluation Results
The models were evaluated on both accuracy and balanced accuracy metrics. The balanced accuracy is calculated as the average of recall (sensitivity) for each class, providing a fair assessment of model performance, especially with imbalanced data.

Below are the results:

| Model               | Accuracy | Balanced Accuracy |
|---------------------|----------|-------------------|
| Logistic Regression | 0.75     | 0.52              |
| Random Forest       | 0.73     | 0.51              |
| Gradient Boosting   | 0.66     | 0.54              |
| K-Nearest Neighbors | 0.59     | 0.48              |
| Linear SVM          | 0.72     | 0.48              |
| Poly SVM            | 0.73     | 0.38              |
| RBF SVM             | 0.76     | 0.46              |
| Sigmoid SVM         | 0.72     | 0.48              |
| Multinomial NB      | 0.62     | 0.54              |
| Complement NB       | 0.53     | 0.55              |
| Bernoulli NB        | 0.67     | 0.51              |

## Tools and Technologies
This project was built using the following tools and technologies:

- **Programming Language**: Python
- **Libraries**: 
  - `pandas` for data manipulation
  - `pickle` for model serialization
  - `re` and `string` for text preprocessing
  - `nltk` and `nlp_id.stopword` for natural language processing and stopword removal
  - `nlpaug` for data augmentation
  - `sklearn` (including SVM, KNN, Gradient Boosting, Naive Bayes variants, Logistic Regression, Random Forest, TfidfVectorizer, GridSearchCV, and model evaluation tools)
  - `warnings` for handling warnings

## Submission

The final submission includes:
- [**Predicted Labels**](https://github.com/steveee27/Multiclass-Text-Classification-of-Presidential-Campaign-Tweets/blob/main/jawaban_penyisihan_bdc_2024.csv): For the unlabeled dataset in the prescribed CSV format.
- [**Code**](https://github.com/steveee27/Multiclass-Text-Classification-of-Presidential-Campaign-Tweets/blob/main/code.ipynb): All scripts used for data processing, model training, and evaluation.


## License

This repository is licensed under the MIT License. You are free to use, modify, and distribute this project with proper attribution. For more details, refer to the [LICENSE](LICENSE) file.

## Acknowledgements

This project is a part of the Big Data Challenge Satria Data 2024. We would like to thank the organizers for providing this challenging and educational opportunity.

## Contributing

While the models developed show promise, the balanced accuracy results are still lower than desired, particularly in handling imbalanced data. We welcome any contributions, whether in the form of improving model performance, experimenting with different techniques, or even just offering suggestions and feedback. Your expertise and creativity could help take this project to the next level. Feel free to fork the repository, submit pull requests, or reach out if you're interested in collaborating!

## Contributors
- [Steve Marcello Liem](https://github.com/steveee27)
- [Marvel Martawidjaja](https://github.com/marvelm69)
- [Matthew Lefrandt](https://github.com/MatthewLefrandt)
