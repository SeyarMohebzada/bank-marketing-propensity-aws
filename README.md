Bank Marketing Propensity: From Legacy to Champion
This is a project where I took a bank’s "legacy" marketing model and gave it a major upgrade using emsable models in AWS SageMaker and resampling techniques.

The Mission
Banks waste a lot of time calling the wrong people. I wanted to see if we could use machine learning to predict exactly who is actually going to subscribe to a term deposit.

What I Did
The Baseline: Started with a "Legacy" Logistic Regression model (it was okay, but missed a lot of opportunities).

The Upgrade: Benchmarked a "Champion" suite of models: Random Forest, LightGBM, and XGBoost.

The Secret Sauce: I used SMOTE to balance the data. Before this, the models were just guessing "No" because they didn't have enough "Yes" examples to learn from.

The Results
Champion Crowned: XGBoost (with SMOTE) is the winner, with a much stronger F1-Score (0.398) re-cross-validated for sanity.


Speed: The entire pipeline runs in just 14 seconds on AWS.

Key Insights (The "Why")
The model showed that these are the biggest drivers for a "Yes":

Past Wins: If they’ve subscribed before, they’re likely to do it again (poutcome_success especially with more frequent 'campaign').

Wallet Size: People with higher balance are much more inclined to commit.

Timing: When you call matters—certain months outperform others by a mile.

How to Run
Upload the .ipynb to an AWS SageMaker Notebook instance and use AWS S3 bucketing for storage.

Run the cells (and don't forget to restart the kernel after the pip install cell!).
