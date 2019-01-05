# Music Box user churn analysis and recommender
## Process: Label generation, frequency feature generation, modeling, and recommender.<br />
### Data info: <br />
           0. event dataset, 12252920 records, 4 fields (uid|event| song_id|date) 
           1. play dataset, 10863763 records, 5 fields (uid|device|song_id|date|play_time|song_length)
### Description: <br />
           0. define the user who is active in label window (between 2017-04-29 ~ 2017-05-12) as 0, otherwise 1.
           1. generate the frequency features for one event type and one time window.
           2. get the device of each user from play dataset.
           3. create a new data frame with all uid and generated features.
           4. fit with Logistic Regression, Random Forest, Gradient Boost Trees models, and Neural Network.
           5. the Random Forest got the highest AUC score which is 0.89.
           6. build popularity recommender, item-item similarity recommender, NMF item-item similarity recommender, and ALS recommender.
