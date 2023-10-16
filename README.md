<br/>
<p align="center">
  <a href="https://github.com/erkutkoral/Virus-Classification">
  </a>

  <h3 align="center">Virus Classification with XGBoost</h3>

  <p align="center">
    Virus Classification with XGBoost.
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/Virus-Classification"><strong>Explore the docs »</strong></a>
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/Virus-Classification/issues">Report Bug</a>
    .
    <a href="https://github.com/erkutkoral/Virus-Classification/issues">Request Feature</a>
  </p>
</p>

![Contributors](https://img.shields.io/github/contributors/erkutkoral/Virus-Classification?color=dark-green) ![Issues](https://img.shields.io/github/issues/erkutkoral/Virus-Classification) 

## Table Of Contents

* [About the Project](#about-the-project)
* [Technologies-Libraries-Frameworks](#technologies-libraries-frameworks)
* [Roadmap](#roadmap)
* [Conclusion](#conclusion)
* [Authors](#authors)

## About The Project

There 4 dimensional (4 feature) numerical inputs (signatures) with labels! We need a simple model that takes these inputs and labels them (Virus, Not a Virus)


## Technologies-Libraries-Frameworks

Python Libraries: Numpy, Pandas, Matplotlib, Seaborn, Scikit-Learn

## Roadmap

1. Visualize the data.
2. Clean up the data.
3. Visualize the cleaned data.
4. Create a simple model that performs reasonably well.
5. Evaluate the model with a test set you will create from the dataset.

## Conclusion
- **Exploratory Data Analysis Insights:**
  - Feature1 is tend to be False/nonVirus.
  - Feature2 is tend to be True/Virus.
  - Feature3 is tend to be True/Virus.
  - Feature4 is tend to be False/nonVirus.
 
  - According to the 4 strip plot, we can see there must be some relationships with the same tending types.
  - With this vision we can check it out with scatter plots with a regression line.
  - We can validate when feature_1 is increasing and feature_2 is increasing too and both of them are related with False output in the starting points and ending points of the line.
  - But we can not say the same things for feature_2 and feature _3. In both parts, there is no strong relationship with false and True. One more thing is interesting too which is the False part of 2 and 3. Because almost the same values for both features make False output.
  
- **Preprocessing Insights**:
  - Feature_1 and Feature_4 are right skewed and have no outliers.
  - Feature_2 and Feature_3 have no skewness and they have outliers.
  - In Feature_2 and Feature_3 there are some outliers but I do not want to detect and delete these outliers. Because this is not an age feature or something like that. We do not know how these parameters works so these outliers may change reaction of output. Moreover, maybe each feature be a symbol of unique transaction.

- **XGBoosst Insights:**:
  - True Positives: In 162 observations we predicted it was a virus and it was true.
  - False Positives: In 36 observations we predicted it was a virus but it was not true.
  - False Negatives: In 38 observations we predicted it was not a virus but it was not true.
  - True Negatives: In 364 observations we predicted it was not a virus and it was true.
 
  - Recall	Precision	F1 Score	Accuracy
    XGBOOST	0.81	0.818182	0.81407	0.876667
 
- **Possible improvements and future work**:
  - Our model seems reasonable but maybe we have more effective models in other folds of our data. In our train-test-split part I used traditional methods for this case. This process is dividing data to train and test set but we do not know which part of our data chosen. In k-Fold Cross Validation we can divide our data into different folds and can run models in those folds to see our model's performance.
  - We did not remove any outliers in Feature_2 and Feature_3 so maybe it makes sense to remove those outliers from our dataset.
  - We used XGBoost in our project but we can try different classification algorithms and check how performance changes from model to model. I chose it from my past experiences but maybe other classification algorithms would make a more effective impact.
  - Last but probably not least, we used XGBoost but did not make any hyperparameters selection or tuning process. It is possible to dig more deeper for hyperparameters could be very efficient but moving to this stage will make the model complicated. In order to keep our model simple I stopped in here. Also the tuning process is very costly for individual people. Conversely, there are good methods for tuning like Bayesian Search with Optuna is a great choice. On the other hand, GridSearchCV is so time consuming and costly but if you need guaranteed better performance this must be the way. In addition to these methods, RandomizedSearch is useful too but it can not guarantee the optimal result.


## Authors

* **Erkut Koral** - [LınkedIn](https://www.linkedin.com/in/erkutkoral/)
