![](https://github.com/JoelTanSG/Classify-Misogyny-in-Database/blob/main/Classifying%20misogyny.png)

![GitHub last commit](https://img.shields.io/github/last-commit/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database)
![GitHub issues](https://img.shields.io/github/issues-raw/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database)
![GitHub](https://img.shields.io/github/license/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database?label=license)
![GitHub top language](https://img.shields.io/github/languages/top/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database)

# Table of Content

- [Project Overview](#project-overview)
    + [Libraries Used](#libraries-used)
    + [Dataset](#dataset)
    + [Features of the final dataset](#features-of-the-final-dataset)
- [WordCloud Analysis](#wordcloud-analysis)
- [Machine Learning and Predictions](#machine-learning-and-predictions)
- [Author](#author)

# Project Overview
Using a dataset created for automatically detecting online misogynistic speech, I set out to clean it up, perform a wordcloud analysis and finally apply machine learning models to look out for misogynistic speech in a database.

### Libraries Used
* pandas 
* pathlib 
* wordcloud
* matplotlib
* scipy.sparse
* sklearn


### Dataset
This dataset is gotten from the publication: [Data set for automatic detection of online misogynistic speech](https://www.sciencedirect.com/science/article/pii/S2352340919305773) by Theo Lynn, Patricia Takako Endo and team.

[Dataset](https://md-datasets-cache-zipfiles-prod.s3.eu-west-1.amazonaws.com/3jfwsdkryy-3.zip)

### Features of the final dataset

Columns|Type|Definition
---|---|---
Definition|object|phrases that might be consider misogynistic 
is_misogyny|float64|either 0.0 for False or 1.0 for True
cleaned_definition|object|a cleaned up of the phases and filtering out stop words

# WordCloud Analysis
Comparison between Non-misogynist definitions and Misogynist definitions

![](https://github.com/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database/blob/main/wordclouds.png)

# Machine Learning and Predictions

# Author

[JoelTanSG](https://github.com/JoelTanSG)
