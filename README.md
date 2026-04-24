# PredictUFC328

This project uses Logistic Regression to predict the outcome of the fight between Khamzat Chimaev and Sean Strickland, set to take place in UFC 328, based on historical fight data.

# Files:

Fighters CSV attributes:
- Name 
- Age 
- Height (cm)
- Reach (cm)
- Wins
- Losses
- Significant strikes landed per minute
- Significant striking accuracy 
- Significant strike defense
- Significant strikes absorbed per minute
- Average takedown landed per 15 minutes
- Takedown accuracy
- Takedown defense
- Average submissions attempted per 15 minutes

Fighters record CSVs - ChimaevFights (for Khamzat Chimaev) and StricklandFights (for Sean Strickland):
- Fight (Opponent) 
- Belt (1 = Title fight, 0 = regular fight)
- Won (1 = won, 0 = lost)
- KO/TKO/Submission (1 = Yes, 0 = Decision)
- Fight time (min)
- Significant strikes landed 
- Opponent's significant strikes 
- Significant strikes landed % 
- Takedowns
- Takedown accuracy
- Control time (min)
- Opponent's takedowns
- Opponent's takedowns accuracy 
- Opponent's control time (min)

DataCleaning Jupyter Notebook:

File for data cleaning and preparation, organizing data and adjusting it so the model can predict adequately.

Models Jupyter Notebook:

File for the model creation, training and prediction, returns the predicted result of the fight.

# Model description

- Model: Logistic Regression
- Penalty: L1
- Solver: Liblinear
- Tolerance: 1e-3

Hyperparameters were initially set and later evaluated using cross-validation.

The model was limitated in 3 fields:
- Extremely small dataset (especially for Chimaev)
- Results are highly sensitive to small variations in data, due to the size of the dataset
- Class imbalance (Chimaev unbeaten)

For prediction, there were 4 options of datasets

Option 1 - Strickland dataset, with himself as sample:


Model predicts Khamzat Chimaev as winner, with 62.78% estimation probability.

Option 2 - Strickland dataset, without himself as sample:


Model predicts Khamzat Chimaev as winner, with 52.73% estimation probability.


Option 3 - Chimaev dataset, with himself as sample:

Model predicts Sean Strickland as winner, with 89.68% estimation probability. This divergence from the other cases
happens because Chimaev dataset has much less samples than Strickland's.


Option 4 - Chimaev dataset, without himself as sample:

Model is not able to predict because Chimaev dataset does not presents two classes, due to the fact that Chimaev
has not lost a fight in MMA until this moment, therefore, the column "Won" only presents value '1'.

# Sources

Data source:
http://www.ufcstats.com/statistics/events/completed

The data were obtained from public sources available for non-commercial, only educational uses.

Predicted probabilities should not be interpreted as real-world likelihoods.

