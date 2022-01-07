![](https://github.com/JoelTanSG/Classify-Misogyny-in-Database/blob/main/Classifying%20misogyny.png)

![GitHub last commit](https://img.shields.io/github/last-commit/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database)
![GitHub issues](https://img.shields.io/github/issues-raw/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database)
![GitHub](https://img.shields.io/github/license/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database?label=license)
![GitHub top language](https://img.shields.io/github/languages/top/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database)

# Table of Content

- [Project Overview](#project-overview)
    + [Libraries Used](#libraries-used-in-this-project)
    + [Machine Learning Models](machine-learning-models-used-in-this-project)
    + [Dataset](#dataset)
    + [Features of the final dataset](#features-of-the-final-dataset)
- [WordCloud Analysis](#wordcloud-analysis)
- [Machine Learning](#machine-learning-models-and-their-results)
- [Model Testing and conclusion](model-testing-and-conclusion)
- [Author](#author)

# Project Overview
Using a dataset created for automatically detecting online misogynistic speech, I set out to clean it up, perform a wordcloud analysis and finally apply machine learning models to look out for misogynistic speech in a database.

### Libraries used in this project
* pandas 
* pathlib 
* wordcloud
* matplotlib
* scipy.sparse
* sklearn

### Machine Learning Models used in this project
* DummyClassifier
* Logistic Regression
* DecisionTreeClassifier
* RandomTreeClasifier


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

# Machine Learning Models and their results

Model|F1 Score|Accuracy Score
---|---|---
DummyClassifier|50.6%|55.24%
LogisticRegression|84.73%|87.34%
DecisionTreeClassifier|83.75%|84.50%
**RandomTreeClassifier**|**86.50%**|**88.21%**

With the RandomTreeClassifier being the clear winner in this project, here is it's confusion matrix:

__|Predicted: False|Predicted:True
---|---|---
Actual: False|231|20
Acutal: True|34|173

And the top 5 most importance features

feature	|importances
---|---
vagina	|0.088365
female	|0.079378
pussy	|0.057255
woman	|0.042098
dick	|0.021577

# Model Testing and conclusion

After running a mix bag of statements, the model was only able to predict correctly 2 out 0f 5 statements.
![](https://github.com/JoelTanSG/Data-Science-Project-Classify-Misogyny-in-Database/blob/main/Model_test_SS.png)

One of the correct predictions had 3 out of the 5 words classified as misogynistic.
It looks like unless the the statement or text has the specific word(s) in the sentence, the model would not classify it as misogynist. Or a single word in the sentence could be taken out of context. Perhaps feeding the model with whole phrases instead would be a better way to train the model. Although that would allow single misogynist words to slip through.

# Author

[JoelTanSG](https://github.com/JoelTanSG)
