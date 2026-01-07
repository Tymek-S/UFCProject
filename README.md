# UFC Project
## Description
This project uses a machine learning model to predict the winner of UFC fights based on historical fights and fighters data (all events from 1996-2024, link below). The goal was primarily learning and personal development. Much of the initial code was generated with the help of AI, but I adapted and customized it to fit my dataset and better understand the modeling process. This project reflects my early steps into data science and machine learning.
## Exploratory Data Analysis (EDA)
EDA was relatively straightforward. I selected the most relevant and easily available fighter parameters. The dataset was already clean, so minimal preprocessing was required. I created several visualizations to explore the data, although no strong patterns were observed, which is common when starting with a new dataset. I converted categorical columns to numeric and removed women’s fights due to the limited number of examples (1–2 per event).
## Creating the Model
I chose a Random Forest model because it is well-suited for this type of problem and a good starting point for learning. I applied a chronological train-test split so the model learns from older fights and is tested on newer ones, which is important for statistics like wins and losses.

I tuned the model’s hyperparameters and set the decision threshold to 0.5. I also created a bar plot to visualize feature importance and explored probabilistic metrics such as Brier Score and Calibration Curve, with guidance from ChatGPT, to better understand the predicted probabilities.

**Model Performance:**
- Train size: 4560, Test size: 1140
- Accuracy: 0.716
- Precision: 0.745
- Recall: 0.785
- F1 Score: 0.765
- Brier Score: 0.202
- Brier Score (calibrated): 0.19

**Confusion Matrix:**
- [[290 180]
- [144 526]]


## Note
This project is a learning exercise. I am just starting out in data science, so there may be mistakes or areas for improvement.
## Data Source
UFC Fights dataset on Kaggle (CC0: Public Domain):
https://www.kaggle.com/datasets/maksbasher/ufc-complete-dataset-all-events-1996-2024
