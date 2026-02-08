Bank Marketing Propensity: From Legacy to Champion
Hey! This is a project where I took a bank’s "legacy" marketing model and gave it a major upgrade using AWS SageMaker and some smart data science.

The Mission
Banks waste a lot of time calling the wrong people. I wanted to see if we could use machine learning to predict exactly who is actually going to subscribe to a term deposit.

What I Did
The Baseline: Started with a "Legacy" Logistic Regression model (it was okay, but missed a lot of opportunities).

The Upgrade: Benchmarked a "Champion" suite of models: Random Forest, LightGBM, and XGBoost.

The Secret Sauce: I used SMOTE to balance the data. Before this, the models were just guessing "No" because they didn't have enough "Yes" examples to learn from.

The Results
Champion Crowned: XGBoost (with SMOTE) is the winner, with a much stronger F1-Score (0.398).

Massive Discovery: We tripled the "Recall" of our legacy model—meaning we're now catching 3x more subscribers than before.

Speed: The entire pipeline runs in just 14 seconds on AWS.

Key Insights (The "Why")
The model showed that these are the biggest drivers for a "Yes":

Past Wins: If they’ve subscribed before, they’re likely to do it again (poutcome_success).

Wallet Size: People with higher balance are much more inclined to commit.

Timing: When you call matters—certain months outperform others by a mile.

How to Run
Upload the .ipynb to an AWS SageMaker Notebook instance.

Ensure your data is in an S3 Bucket.

Run the cells (and don't forget to restart the kernel after the pip install cell!).
