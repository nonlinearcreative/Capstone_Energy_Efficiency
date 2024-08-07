# Predicting whether or not a structure is energy efficient based on features in the data. 

# IMPORTANT: There are two notebooks in this repository. One contains the working explorations related to the study, model variations, and analysis visualizations. The other is a 'model only' notebook intended for the end-user. 



by Jim O'Donnell

#### Capstone project analyzing energy efficiency of residential buildings. 

#### Executive Summary: 


## Rationale
This study aims to create and fine tune a model for understanding and predicting the features which contribute to inefficient energy usage for both heating and cooling a structure.

## Research Question
Will the model be able to accurately rate a real-world structure using a binary classification as having either High heating load or not, or High cooling load or not?

## Data Sources:
https://www.kaggle.com/datasets/ujjwalchowdhury/energy-efficiency-data-set/data

## Goals: 
To produce a low friction end-user interface which takes manual entry of available data features, runs the input through two algorithms, makes predictions of the targets, and finally classifies the entry as either efficient or inefficient for both heating as well as cooling loads based on the input data. The interface must be simple enough for anyone to use.  

## Findings: 
The study took a two-phased approach by first defining two separate target features, heating and cooling load, analyzing them as two separate studies, and developing models to both predict heating and cooling loads as well as a binary classification of 'efficient' or 'inefficient' based on the input data. 

## Scores: 
The mean cross-validated score for heating load prediction using Random Forests: 0.9973197960731153
The mean cross-validated score for cooling load prediction using Random Forests: 0.9676260412022117

The mean cross-validated score for heating efficiency classification using Logistic Regression: 0.9837265093962415
The mean cross-validated score for cooling efficiency classification using Logistic Regression: 0.9869518859123018 

(quite high, indeed!)

## Learnings: 
Early on, Random Forests performed exceptionally well over the other models I tested for predicting the  heating and cooling load target features. When I began to use it for classification of 'efficient' versus 'inefficient', cross-validation scores indicated overfitting. This prompted a search for a less complex model for classification. Logistic Regression emerged as a strong candidate. I ultimately found that by combining the two models, I could build an uber simple user interface that anyone could use that would output highly accurate prediction results without mucking about in the code. 

## Stretch goals: 
* The (model only) notebook should be so easy to use, domain experts should be able to use it even if they don't look at the README.
* Make a Python file that runs the model in a terminal window.  


## Next Steps: 
Research how to gather the raw data about a structure in the wild and run that new data through this model. Explore ways to add more granular data features to these models. 










## Archive:



## Methodology: 
(Planned as of 7/1/2024) Data cleaning and analysis - including pairplots of the data against the target features, heatmaps of correlations between the features, in-depth analysis of features with identifiable patterns when plotted against the target features, model building, testing, and hyperparameter tuning, and finally sourcing and introducing real-world data into the model. 
## Results
(7/1/2024) Too early to provide results or actionable recommendations. More detailed notes on current progress provided in the notebook.
## Next Steps
(7/1/2024) Continue working on handling multicollinearity, analyze feature importance, experiment with PolynomialFeatures and analyze results, build and evaluate some classification models (Logistic Regression, KNN, RandomForest). 



June 4, 2024
Original Problem statement: 

        Research Question:
        With a thorough understanding of measuring and rating home energy efficiency using this dataset, how well will my models perform when I add real-world data (in this case, all corresponding inputs related to my home)?

        The data:
        The dataset I am using Links to an external site.comes from Kaggle. It was generated by simulating 12 different building shapes in Ecotect. Further simulation based on functions related to glazing area, orientation, surface area, as well as other features expand the dataset to 768 building shapes. The data aims to predict two real-valued outcomes (heating load and cooling load).

        The process:
        I will first conduct extensive data cleaning and analysis (already in progress) and get to know the dataset completely and how it performs using a variety of models. Next, I will do some independent research on how to measure the corresponding input data on my house.

        Early pairplots have revealed some nice bell curves and isolated clusters of data. I will be experimenting with Logistic Regression, KNN, and RandomForest for classification. I have also started using GridSearchCV to identify feature importance. 

        Expected results:
        I can honestly say at this point, I have no idea what to expect. My hope is that I can take this experiment further than I have been able to with the Practical Application assignments. I want to feed real-world data into my models and achieve some measure of verifiable accuracy. There are a fair number of unknowns at this point – namely how to understand and gather the data about my house. But that is a stretch goal. The goal of the assignment is to build a solid and flexible notebook

        Why this question is important:
        On a micro scale, my house loses heat like crazy. Studying the nature of the heat loss and gathering (historical) data will help me identify areas that can be improved upon to reduce heat loss. I believe there will be correlations to Heating Load in my dataset.

        On a macro scale? I’m not thinking about this at large scale at this point. I also lack domain expertise and do not have a lot of domain intuition to bring to this – it is more of a personal interest of mine. But in an ideal situation, a study such as this could have definite benefits to commercial and residential heating and cooling optimization methods.
