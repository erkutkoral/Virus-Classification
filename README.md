<br/>
<p align="center">
  <a href="https://github.com/erkutkoral/KMeans-Hierarchical-Clustered-Retail-RFM">
    <img src="https://www.slidesalad.com/wp-content/uploads/2020/07/RFM-Customer-Segmentation-Model-PowerPoint-Templates-Slides.jpg" alt="Logo" width="400" height="400">
  </a>

  <h3 align="center">KMeans and Hierarchical Clustered RFM Analyisis with Retail Data</h3>

  <p align="center">
    Performed RFM Analysis in Retail Data and Created clusters with KMeans and Hierarchical Clustering methods to gain insights and compare them.
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/KMeans-Hierarchical-Clustered-Retail-RFM"><strong>Explore the docs »</strong></a>
    <br/>
    <br/>
    <a href="https://github.com/erkutkoral/KMeans-Hierarchical-Clustered-Retail-RFM/issues">Report Bug</a>
    .
    <a href="https://github.com/erkutkoral/KMeans-Hierarchical-Clustered-Retail-RFM/issues">Request Feature</a>
  </p>
</p>

![Contributors](https://img.shields.io/github/contributors/erkutkoral/Titanic_Classification?color=dark-green) ![Issues](https://img.shields.io/github/issues/erkutkoral/KMeans-Hierarchical-Clustered-Retail-RFM) 

## Table Of Contents

* [About the Project](#about-the-project)
* [Technologies-Libraries-Frameworks](#technologies-libraries-frameworks)
* [Roadmap](#roadmap)
* [Conclusion](#conclusion)
* [Authors](#authors)

## About The Project

![About the Project](https://www.responsedga.com/wp-content/uploads/2021/02/Incontent_image.png)

The data set named Online Retail II includes the online sales activities of a UK-based retail company between 01/12/2009 and 09/12/2011. The product catalog includes souvenir products and it is known that many customers are wholesalers.
Analyzing customer behavior in this retail data with the RFM method and perform clustering.


## Technologies-Libraries-Frameworks

Python Libraries: Numpy, Pandas, Matplotlib, Seaborn, Scipy, Datetime, StandardScaler, KElbowVisualizer, AgglomerativeClustering.

## Roadmap

1. Exploratory Data Analysis
2. Handling Missing Values
3. Creating RFM
4. Handling Outliers
5. KMeans Clustering
6. Hierarchical Clustering

## Conclusion
- **Exploratory Data Analysis Insights:**
  - Quantity and Price variables have negative values.
  - There is a large difference in product quantities and prices between the minimum values and the 1% sample.
  - A large value difference was observed between 99% of the sample and max values of the same variables.
  
- **Preprocessing Insights**:
  - Recency variable has outliers but it can not be seen in %5 - %95 parts of data.
  - For not changing dataset patterns we are looking in that range if we go up for more we may change decriptive metrics and it is going to change distribution of data. This is not a situation we want.
  - All variables have right skewed distribution. We want our variables to be close to normal distribution. The reason for this is to disseminate the observations and transform them into a form that can be expressed more easily. Used Log Transformation for these purposes.

- **KMeans Insights:**:
  - Utilized Elbow method for optimizing cluster numbers.
  - The lowest distance error was seen in the 8-cluster structure with sum of squares.
  - Monetary structures of the 5th segment and the 7th segment have similar average, median and observation values. There may be a thought as to whether these should be combined.
  - As we continue to observe these segments, Frequency structures also show similar metrics.
  - However, the shopping frequency structure (Recency) of these customers is different and these clusters are separated at this point. The 5th segment is based on old customers, but the 7th segment has newer customers.
  - The segment with the highest money spending is seen as the 4th segment. There may be special campaigns for this segment.
  - Similarly, the segment with the lowest spending is segment 1 and these customers have not made any purchases recently. Their frequencies also have the lowest values. There may be special campaigns for these customers.
 
- **Hierarchical Clustering Insings**:
  - Created the hierarchical clustering structure in a unifying way from the general to the specific and increase the number of clusters to 10 to see what we have when we increase the clusters from 8.
  - Among the 10 classes, the 4 yellow classes which means these clusters are way more smilar than the other and can be combined for reducing to 6 classes.
  - Classes 2 and 4 are very similar in terms of the amount of money spent. Is it possible to combine these classes?
  - They have similar Monetary and Frequency values, but they differ in terms of when the customers last shopped. The shopping made by class 2 can be classified as very old and even we can make this class lost, but class 4 is much more recent.
  - Class 5 is very valuable. Max. value for money is in this class. Customers shopped very frequently and made purchases very recently.
  - As an important point, the least number of customers is in the 5th grade.
  - Most customers are in the 2nd class, but mentioned that this customer class can be classified as lost. Efforts can be made to keep these customers up to date.


## Authors

* **Erkut Koral** - [LınkedIn](https://www.linkedin.com/in/erkutkoral/)
