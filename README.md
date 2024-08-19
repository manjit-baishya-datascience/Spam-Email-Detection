# **Spam Email Detection**
![Asset 2](https://github.com/user-attachments/assets/ef019c7e-b82a-4aee-bacd-e7b69567f7ec)


## **Overview**
Spam Email Detection is a critical feature for improving user experience and security by automatically identifying and filtering out unwanted emails. This project demonstrates how to build a spam detection system using Natural Language Processing (NLP) and machine learning techniques.

## **Project Structure**
This project is organized into several key components:

- **Data**: A dataset of emails labeled as spam or ham (non-spam).
- **Preprocessing**: Steps to clean and prepare the email data for modeling.
- **Modeling**: Machine learning algorithms used to classify emails.
- **Evaluation**: Assessing the performance of the models.
- **Pipeline**: A complete pipeline from data preprocessing to prediction.
- **Testing**: Examples of how the model performs on new, unseen emails.

## **Data**
The dataset contains two main columns:
- `Category`: Indicates whether the email is `spam` or `ham`.
- `Message`: The actual content of the email.

The data is loaded from a CSV file and initially explored to understand its structure and content.

## **Data Preprocessing**
Effective preprocessing is essential for building a reliable spam detection model. The preprocessing steps include:

1. **Lowercasing**: Converting all text to lowercase ensures uniformity, making the model less sensitive to case variations.
2. **Removing Punctuation**: Punctuation marks are typically not useful for spam detection and are removed to simplify the text.
3. **Removing Non-Alphabetic Characters**: This step eliminates numbers and special characters, focusing on the meaningful words.
4. **Tokenization**: Breaking down each email into individual words (tokens) to analyze the text more effectively.
5. **Removing Stop Words**: Common words like "and," "the," and "is" are removed since they do not contribute significantly to the classification.
6. **Lemmatization**: Reducing words to their root form (e.g., "running" to "run") ensures that different forms of a word are treated as the same.

## **Modeling**
The processed data is then used to train a machine learning model. In this project, we use the **Extra Trees Classifier**, a powerful ensemble learning method that combines the predictions of multiple decision trees for more accurate results.

### **Key Steps in Modeling:**
- **Vectorization**: Transforming the text data into numerical format using techniques like TF-IDF (Term Frequency-Inverse Document Frequency).
- **Training**: The model is trained on the processed and vectorized data.
- **Oversampling**: Since spam emails are less frequent in the dataset, oversampling is applied to balance the classes and improve model performance.

## **Evaluation**
The model's performance is evaluated using metrics such as accuracy, precision, recall, and F1-score. A confusion matrix is also plotted to visualize how well the model distinguishes between spam and ham emails.

## **Pipeline**
A complete pipeline is created to automate the entire process, from data preprocessing to making predictions on new emails. This pipeline can be easily integrated into email systems to provide real-time spam detection.

## **Testing the Model**
The model is tested with a variety of sample emails to demonstrate its effectiveness. For each email, the model predicts whether it is spam or ham, with results that align well with expectations.

### **Example Predictions:**
- "Congratulations! You've won a $1000 Walmart gift card. Click here to claim your prize now!" - **Predicted as Spam**
- "Don't forget our meeting at 3 PM today. Looking forward to discussing the new project." - **Predicted as Ham**

## **Conclusion**
This project successfully implements a spam email detection system using NLP and machine learning. The system is accurate and efficient, making it a valuable tool for enhancing email security and user experience.

## **Requirements**
To run this project, you'll need to install the necessary Python libraries:
- pandas
- matplotlib
- seaborn
- scikit-learn
- imblearn
- nltk
