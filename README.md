# Advanced-Modeling-Customer-Purchase-Prediction


This repository contains the analysis and modeling for customer purchase predictions using various statistical methods. The project focuses on developing and comparing Poisson, NBD, Zero-Inflated NBD, and Finite Mixture Models to predict customer purchases based on historical data. It also includes a second part where regression models are applied to predict the number of publications by doctoral candidates using a set of predictors.

## Project Overview
The project consists of two main parts:

## Part I: Customer Purchase Prediction (Candy Data)
In this section, several models are developed and evaluated using the candy.csv dataset:

Poisson Model: A basic model to understand the underlying purchase distribution.

NBD Model: A Negative Binomial Distribution model that accounts for overdispersion in the data.

Zero-Inflated NBD Model: This model assumes two types of customers — non-buyers and eventual buyers, using a mixture of zero inflation and NBD.


Finite Mixture Models: Models with 2, 3, and 4 segments to capture heterogeneity in the customer base, offering predictions for different customer groups.
We evaluated the models based on log-likelihood values, AIC, and BIC criteria to select the best-performing model.

## Key Insights:
The 3-segment Finite Mixture Model offers the best balance between complexity and predictive performance based on AIC and BIC.
Poisson models performed poorly, indicating that overdispersion is present in the data and needs to be addressed.

## Part II: Predicting Doctoral Candidates' Publications (Articles Data)
In this section, we predicted the number of publications by doctoral candidates using the articles.csv dataset, incorporating various independent variables:

Poisson Regression: A standard model for count data.
NBD Regression: Used to model overdispersed count data.
Zero-Inflated NBD Regression: Combines zero-inflation with NBD to account for candidates who may never publish.
## Key Insights:
The NBD Regression performed the best, with the lowest AIC and BIC values.
Significant predictors include marital status, department prestige, and mentor publications. Candidates who are married and from prestigious departments with more publications by their mentors are likely to publish more.
## Datasets
### candy.csv: Customer purchase data for building and evaluating different purchase prediction models.
### articles.csv: Data on doctoral candidates' publication records along with demographic and academic factors.
Notebooks
The code and analysis are provided in Jupyter notebooks for each section of the project. Detailed comments and explanations are included to make the code easily understandable and reproducible.

## How to Run the Project
## Clone the repository:
git clone https://github.com/Venkyy97/Advanced-Modeling-Customer-Purchase-Prediction.git

## Install the necessary packages:
pip install -r requirements.txt

Open the Jupyter notebooks and run the cells to reproduce the analysis and visualizations.
