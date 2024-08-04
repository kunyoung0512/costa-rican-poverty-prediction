# costa-rican-poverty-prediction
Kaggle competition on Costa Rican poverty

# Description
The Inter-American Development Bank is asking the Kaggle community for help with income qualification for some of the world's poorest families. Are you up for the challenge?

Here's the backstory: Many social programs have a hard time making sure the right people are given enough aid. It’s especially tricky when a program focuses on the poorest segment of the population. The world’s poorest typically can’t provide the necessary income and expense records to prove that they qualify.

In Latin America, one popular method uses an algorithm to verify income qualification. It’s called the Proxy Means Test (or PMT). With PMT, agencies use a model that considers a family’s observable household attributes like the material of their walls and ceiling, or the assets found in the home to classify them and predict their level of need.

While this is an improvement, accuracy remains a problem as the region’s population grows and poverty declines.

To improve on PMT, the IDB (the largest source of development financing for Latin America and the Caribbean) has turned to the Kaggle community. They believe that new methods beyond traditional econometrics, based on a dataset of Costa Rican household characteristics, might help improve PMT’s performance.

Beyond Costa Rica, many countries face this same problem of inaccurately assessing social need. If Kagglers can generate an improvement, the new algorithm could be implemented in other countries around the world.

This is a Kernels-Only Competition, so you must submit your code through Kernels, rather than uploading .csv predictions. You can create private Kernels and even share/edit your work with teammates by adding them as collaborators.

# Data Preprocessing
- Overview of Data
- Exploratory Data Analysis
- Filling up discrepancies in data (Filling up Nan values, Replacing “Yes” and “No”, Rectifying erroneous target labels)
- Feature Engineering	(Binary to Ordinal, Aggregating Features, Removing redundancy and decreasing dimensionality)
- Preparing dataset for training

# Experiments & Results
- Models
  1. Bagging classifier
  2. Random Forest classifier
  3. Extra Trees classifier
  4. LightGBM classifier
- Training
  1. Bagging classifier
  2. Random Forest classifier
  3. Extra Trees classifier
  4. LightGBM classifier
- Predicting/Classifying
  1. Bagging classifier
  2. Random Forest classifier
  3. Extra Trees classifier
  4. LightGBM classifier
 
# Conclusion
The LightGBM was chosen as our final classifier as it showed the highest accuracy and f1 score out of all the classifiers. The final results were submitted to the Kaggle competition and the evaluation score and ranking were as follows.

The highest evaluation score returned was 0.40802 and our result will place us at 231/616 position on the leaderboard (top 37.5%). 

Comparing the results in the previous section (figure 22 - 28), we can see that the accuracy scores achieved using the dataset with aggregated statistics across households actually are marginally worse than the scores using the default dataset (individual level). This is contrary to our expectations. These are some of our analysis and explanations as to why the aggregated dataset performed poorly:
  •	The dataset comprising of individual level data contained a lot more data samples and much more robust compared to the aggregated dataset (about 4 times more training samples). More training data will add more diversity to the model training and decreases the generalization error.
  •	The creation of new household level statistical features like ‘min’, ‘max’, ‘sum’, ‘count’, ‘standard deviation’ and ‘range’ may not have improved the model performance. In fact, these extra features could have added more irrelevant noise to the model training, which in turned reduced the model accuracy as the model may not have correlated well with the other original features that the dataset contained. Another explanation is that overfitting might have occurred with the addition of the new created features. 
    o	It is worth noting that number of features that are household aggregated essentially multiplied by 5 (5 statistical methods used). 

![image](https://github.com/user-attachments/assets/fd68e4be-07f3-40c7-bd2d-b52dcb8c3f83)



