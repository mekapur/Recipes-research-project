# Recipes-research-project
Project for DSC 80 at UCSD

Name: Mehak Kapur

Website Link: https://mekapur.github.io/Recipes-research-project/

## Introduction

A treasure trove of culinary inspiration and information, with over 234,000 recipes at your fingertips, this dataset offers a diverse array of dishes spanning cuisines, flavors, and cooking styles. In this project we are exploring the relationship between the number of calories and the average rating of a dish. 

This data set contains :

No of rows : 234429 rows 

No of cols : 18 columns

Cols relevant to question: 

name - The name of the dish in the recipe 

nutrition - The nutritional values like calories, total fat, sugar etc 

ingredients - Ingredients used in making the dish 

description - Use of words like chocolatey, delicious, sweet etc

## Data Cleaning and Exploratory Data Analysis

Description of data cleaning that took place: 

-- For the nutrition column I turned the strings into actual columns of the form in the form calories (#), total fat (PDV), sugar (PDV), sodium (PDV), protein (PDV), saturated fat (PDV), and carbohydrates (PDV). 

-- Looked at how many missing values there are in each column and replaced them with NaN

-- Binned the 'average_rating' values into specified intervals defined by the bins list and assigns corresponding labels from the labels list to each interval.

<iframe
  src="assets/plot1.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>

















