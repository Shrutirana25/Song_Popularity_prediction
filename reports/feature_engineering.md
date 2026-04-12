# Song Popularity Prediction Project –  

## Feature Engineering:-
Here new features are engineered so that they contribute to the prediction of **popularity** :
* party score  = energy x dancebility
* happy dance = valence x dancebility
* mood = valence * energy
* instrulentalness --> yes or no
* tempo --> low medium high
* artist freq --> count of different artists for a track
* artist popularity mean = mean of the popularity ofeach artist envolved in a particular track 
* is collab = did artists collaborated together

## Preprocessing Data:- <br>
* **Missing Value Analysis :-**<br>
*Need*: Models cannot perform when there are missing values and hence shall be removed.<br>
*Observations*: Only three features have one misssing value each. It is possible that these values belong to one particular entry.<br>
*Solution*: The missing values should be dropped.

* **Column Transformation :-**<br>
From the graph analysis we get to know that many features are skewed and need to be transformed<br>
*Need*: Features which are not normally distributed can affect the performance of the models like LINEAR REGRESSION, LOGISTIC REGRESSTION(classification), PCA, KNN. <br>
*Solution*: **Yeo-Johnson** transformation is applied on the features as it can be used on positive as well as negative value of skewness.

* **Multicolinearity :-**<br>
*Need*: In machine learning we assume the features to be independent of each other and only depend on the target feature. If they are not independent that is multicollinearity exists then performace of models like  LINEAR REGRESSION, LOGISTIC REGRESSTION(classification), PCA, KNN will get affected.<br>
*Solution*: Out of the featues that have vif value **>10** any one or more features can be dropped

* **Outlier Analysis :-**<br>
*Need*: If any feature contains more than 5-10% it affects the model performances and hence shall be removed.<br>
*Observations*: Only time signature and instrumentalness have outliers.<br>
&nbsp;&nbsp;&nbsp;&nbsp; **- Instrumentalness:** most of the songs do not have only instrumental music i.e they have vocals too<br>
&nbsp;&nbsp;&nbsp;&nbsp; **- Time_signature:** most of the songs fulfill all the 4 parts. <br>
*Solution*: There is no need to perform any type of outlier analysis

* **Encoding :-**<br>
*Need*: If any feature contains categorical values, the ML models cannot process them. Hence the categorical values need to be converted to numerical.<br>
*Observations*: Only track genre has categorical values that too multiple values(multi-label feature), and all other categorical features have been removed or modified. <br>
*Solution*: To convert the categorical features to numerical features, new features for every label is created and marked as 1 if the track have that genre and 0 if not present. <br>

* **Scaling :-**<br>
*Need*: Features may have values that are different in scale  and may cause the model to interpret the patterns different and hence give bad performance.<br>
*Solution*: The numerical features must be scaled.

* **Converting the processed file to csv file :-**
After all the processing, the resulted table is converted to the csv file so that can be used multiple times.