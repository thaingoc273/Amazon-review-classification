# Amazon-review-classification

Semantic analysis: Classify reviews from Amazon using various methods: Logistic regression, Random Forest, Extreme Gradient Boosting and Long short term memory 

# 1. Dataset 
Dataset from Kaggle, Amazon fine food reviews: https://www.kaggle.com/snap/amazon-fine-food-reviews
 - 568,454 reviews
 - Rating: 1-5 (1 worst, 5 best)
 - Map rating to positive (3-5) and negative (1-2)
 - Percents of position 85% and negative 15%

# 2. Semantic analysis

Use two packages: CountVectorizer and TfidfVectorizer
 - https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html
 - https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html
 
Using these two packages, the reviews are transfered to matricies for inputs of classification problem

# 3. Machine learning methods

- We use Logistic regression, Random forest and Extreme Gradient Boosting. Moreover, we construct simple Long Short Term Memory networks for classification problem.

- Due to unbalanced dataset, we also resample dataset to get balanced. Methods are upsampling and downsampling

# 4. Results
After using various methods, we see that Logistic regression and TfidfVectorizer work well for our problems. We use confusion matrix for evaluation our methods.

Logistic regression runs rather faster than other methods and is easy to intepret by coefficient scores.

- Results for upsampling

         Model Training Accuracy: 0.9976800597332333

         Model Test Accuracy: 0.9508985743839453

         Confusion matrix [[ 15758   4838]
                           [  2140 119378]]

         F1 Score: 0.818724996103289

         Recall: 0.7651000194212468

         Precision: 0.8804335679964241

- Results for Long Short Term Memory network

        Accuracy of the model :  0.9186568868810436
        
        F1-score:  0.6818226943313809
        
        Recall: 0.6088652482269503
        
        Precision: 0.774644710128581
        
        Confusion matrix: [[ 3434  2206]
                           [  999 32762]]

# 5. Future work

- Collecting more data

- Turning hyperparameters for our models. We use default for all models

- Use more deep networks
