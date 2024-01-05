What All I did in this Task? (used pandas library max. + Scikit learn for algorithms + matplotlib and seaborn for visual representation )

EDA Part

-> First , visualizing the data manually I observed that the last two columns are output columns and the remaining are our input columns.

-> Then I searched about what exactly is EDA and how to do it?
Doing this, I found the most important term FEATURE ENGINEERING.

	-> EDA is a part of Feature engineering and it is all about cleaning and preprocessing
 our dataset to make it better for our model training as sometimes data given to us is very raw and random.

-> Cleaning the data involves handling; 

 a. missing values
 b. Identifying irrelevant data/features(columns)
 c. managing outliers is a great task
 d. Trimming and organizing the data in mannered way
 e. Adding new features(columns) based on given , if required to predict better.

EDA part of my task:

First through pandas function info(), I saw there are no missing values.

Then I observed the hear_left,hear_right and urine_protein,sex(won’t affect our model) columns have nearly constant value to 1, which won’t affect our model , so I dropped those features by drop(column=’ ’) method.

The toughest part which I found and took most of my time in researching was HOW TO MANAGE OUTLIERS? - In every feature of a dataset , there are always some outliers and the extent of them depends on how skewed the data is and the distribution.First I find the skewness of each feature(column) ny skew() function . Then for not much(moderately) skewed data i.e. normally distributed data - by IQR technique I removed those outliers from the dataset. And then for high skewness which was positive here , I found some techniques like log transformation and square root transformation to reduce the skewness and get a nearly normal distribution.

Then visualizing I thought that the weight and height are very non judgemental columns , so I made a new feature named bmi-index which is a better way to predict especially in such biological problems and so I removed those 2 columns also.
The final modified dataset is named sdd3 in my task on google colab.

Training Models and evaluation:

Random forests

-> It is like a combination of Decision Trees

Accuracy for smokers: 69%
Accuracy for drinkers: 68%

(once  I obtained 74% (on original data)also for some tuning of hyperparameters)WHY This happened , I still have a doubt!!

The computational speed was very slow as it took 5-10 min to train . 

Decision trees 

-> It's a very extensively used algorithm for tasks of classification and regression training.

Accuracy for smokers:  68%
Accuracy for drinkers: 68%

The computational speed was very fast compared to random forest as it’s only a single tree and took like around 5 to 10 seconds.

Note: I also perform Cross-validation of hyperparameters by Gridsearchcv method but it took too much time to execute


Gradient Boosting

-> It’s an ensemble learning algorithm which trains a model sequentially and the new model tries to correct the previous model.
Ensemble learning - A machine learning model technique that involves combining the predictions of multiple individual models to create a more robust and accurate predictive model.It is basically we can achieve better performance than any single model.

Accuracy for both: 70% 

The computational speed is extremely slow around 45 mins but a good efficiency is achieved.

KNN(K-nearest neighbors) and linear regression are possible ways to evaluate .
But I thought Linear regression is based on the linearity principle and it was hard to find some linearity on such a large dataset.

Comparing Computational speed and efficiency I found Decision Trees model to be the best giving roughly around 70% efficiency in less time and easy to deploy the model faster.





—---------------------------------------------Thank You —-----------------------------------------
