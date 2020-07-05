# Traffic Light Classifier

## Introduction
This project is from Udacity's 'Intro to Self Driving Car' Nanodegree Program - Computer Vision Class. Traditional Computer Vision technique of feature extraction from Image is used to build the classifier.

## Project Goal
The goal of this project is to classify the state of Traffic Light as either _Red, Yellow_ or _Green_ based upon the light which is illuminated.

## Brief Steps
- Load and Visualize data
- Pre-process the data for Standardized Input
- Feature Extraction
- Classification & Accuracy Calculation over Validation Set

> Please refer Traffic_Light_Classifier.ipynb for Detailed Steps and Code.

## Feature Extraction
Two kinds of feature were extracted
1. **Positional Brightness**
- Background from the image is cropped to focus only on traffic light area.
- Image is converted to HSV colorspace so that brightness can be extracted.
- Three areas are defined for each Color class with sum of brightness of defined area as feature value to classify.

2. **Positional Color**
- Color masks are applied to extract required color classes using HSV Color Space.
- Three areas are defined for each Color class with sum of brightness of defined area for respective color masked image as feature value to classify.

### Drawbacks
- Feature 1 - Athough feature 1 was able to achieve **>95%** Accuracy, In some cases background is not fully cropped and position of brightness value is not correct indication of the state of Traffic Light. Due to this 2nd feature is implemented.

- Feature 2 - In some cases it was not possible to extract indicated color from HSV colorspace due to reflection/shadow on the original color. Thus, brightness feature helps in such cases.

Thus, features are designed in such a way that they complement each other's drawbacks and help in right classification of the Traffic Light State.

## Classification and Accuracy
- Classifier Function compares addition of both the feature values for all three classes.
- With the features defined it is able to achieve **100%** Accuracy

## Assumptions

- Traffic lights are oriented vertically with little deviation in angles. 
- Order of lights is Red, Yellow & Green from Top to Bottom.

## Suggestions
Please feel free to comment for any thoughts, suggestions or improvements on the project.

You can also connect with me on [LinkedIn](https://www.linkedin.com/in/chirag-baru-979620a5/) & [GitHub](https://github.com/AnExplorer28)