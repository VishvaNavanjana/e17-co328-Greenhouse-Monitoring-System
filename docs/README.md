---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: eYY-XXX-project-template
title: Greenhouse Monitoring System
---

[comment]: # "This is the standard layout for the project, but you can clean this and use your own template"

# Greenhouse Monitoring System Based on Image Spectral Data

---


## Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Our Solution](#our-solution)
4. [System Modelling](#system-modelling)
5. [Solution Architecture](#solution-architecture)
6. [Software Design](#software-design)
7. [Machine Learning Model](#machine-learning-model)
8. [Team](#team)
9. [Links](#links)

---

## Introduction

Greenhouse Monitoring System provides a platform to manage the Greenhouse by tracking the phases of plant harvest, identifying any plant disorder and tracking the plant growth by using the image spectral data of plants. The system is basically considered the key problems plant diseases, huge harvest wastage and unnecessary expensive maintenance in a greenhouse. So this system will make a high positive impact on maximizing the harvest and reduce maintenance cost in Greenhouses.

![Introduction](./images/introduction.PNG)

## Problem Statement
- Different behaviors of plants under different conditions
- Various disorders of plants
- Taking manual measurements of information of the plants
- Inefficiency of labor system
- Unnecessary higher cost for maintenance

Although the environmental conditions of plants are controlled, the temporal effects like temperature, humidity may not evenly balanced for each crop. Therefore, plants respond differently under those unbalanced environmental conditions. And, plants can have different kind of disorders. It leads to production failures in greenhouses. As well, the crop yield may not be harvested at the right moment. Because of that there would be a huge harvest wastage.

In current greenhouses, the workers continuously observe the plant growth. In that case, workers will be tired and labor system would be inefficient. So, there would be an unnecessary higher cost for maintenance.

![Problems](./images/problems.png)

## Our Solution
Plant diseases, huge harvest wastage and unnecessary expensive maintenance have been observed as the major issues in current Greenhouse Systems. These key problems simulated the development of image analysis and computer vision methods. That's how the "greenhouse monitoring system based on image spectral data" came to the stage.

![Our_solution](./images/camerasystem.PNG)

## System Modelling
### Functional Requirements
- System updates per one hour with new plants images according to the given video file.
- Monitor the diseases, crop harvest and growth plant by plant.
- When displaying the features of the system, user should be able to select plant according to their labels.
- If any error occurred in the system, it should be displayed as an alert.
- When the crop should be harvest at the moment, user should be notified it.
- Monitor the future greenhouse status of the features.
- Reports should be generated and they should be able to download.

### Non-Functional Requirements
- User Interfaces should be user friendly.
- Performance with response time should be efficient.
- The prediction of ML Model should be reliable
- Web Application security should be high.
- In the future, according to new requirements, system sholud be scalable.

### Use Case Diagram
![usecase_diagram](./images/usecase_diagram.PNG)

## Solution Architecture
### System Functionalities
1. Extract images from the video file.
2. Extract features from images.
3. Store those images and features in a database.
4. Data processing and data analysis using ML Model
5. Data Visualization
6. Data Prediction and generate reports

![High_level_diagram](./images/high_level_diagram.PNG)

### System Overview with Technology Stack
![Technology_stack](./images/technology_stack.PNG)

## Software Design
### User's Application Data Flow
![app_data_flow](./images/app_data_flow.PNG)

### User Interfaces
1. Login
  - Greenhouse workers can login to the system by entering username and password.
  ![login](./images/login.PNG)

2. Dashboard
  - User can monitor the overall status of greenhouse
  - User can see what plants have problems in the greenhouse layout panel. and if user clicks the layout it will navigate to the Overview User Interface.
  ![dashboard](./images/dashboard.PNG)
  
3. Overview
  - User can monitor all plants at once.
  ![overview](./images/overview.PNG)
  
4. One Plant Overview
  - User can monitor only one plant
  - If user needs to see the diseases, growth and harvest status of that plant, he can click those options in the user interface
  ![one_plant_overview](./images/one_plant_overview.PNG)
  
5. Leaf Diseases
  - If the plant has any disease it will be shown in this interface.
  ![diseases](./images/diseases.PNG)
  
6. Plant Growth
  - The plant growth can be monitored here.
  ![growth](./images/growth.PNG)
  
7. Crop Harvest
  - The plant harvest status can be seen here.
  ![harvest](./images/harvest.PNG)
  
8. Predictions
  - The predictions of diseases, growth, harvest of each plant can be monitored here.
  ![predictions](./images/predictions.PNG)
  
9. Reports
  - The reports of the greenhouse system status can be seen and downloaded from here.
  ![reports](./images/reports.PNG)


## Machine Learning Model
- The main target of Machine Learning Model is to predict the specfic two main features.
- For a given time period, the crop harvest stage and the leaf diseases are predicted here.

### Leaf Disease Detection
- System defined 10 different kinds of diseases.
  - Tomatomosaicvirus
  - Target_Spot
  - Bacterial_spot
  - TomatoYellowLeafCurlVirus
  - Late_blight
  - Leaf_Mold
  - Early_blight
  - Spidermites Two-spottedspider_mite
  - Tomato___healthy
  - Septorialeafspot
 
#### Leaf Disease Detection Model Architecture
![leaf_diseases_model](./images/leaf_diseases_model.PNG)

### Crop Harvest Stage Prediction
- Separate fruits from the given images
- Detect Average color
- Predict the crop harvest stage and count the number of fruits according to the color bar

![crop_harvest_ml_model](./images/harvest_stage_ml_model.PNG)

### Test Results
#### Leaf Disease Detection
![test_results_1](./images/test_results_1.PNG)

## Team
#### Developers
-  E/17/297, Rupasinghe T.T.V.N., [e17297@eng.pdn.ac.lk](mailto:e17297@eng.pdn.ac.lk)
-  E/17/206, Manohara H.T., [e17206@eng.pdn.ac.lk](mailto:e17206@eng.pdn.ac.lk)
-  E/17/148, Kalpana M. W. V., [e17148@eng.pdn.ac.lk](mailto:e17148@eng.pdn.ac.lk)

#### Scrum Master
- Ms. Kalani Hansima

#### Product Owners
- Dr. Asitha Bandaranayake
- Mr. Prabhath Gunathilake

## Links

- [Project Repository](https://github.com/cepdnaclk/e17-co328-Greenhouse-Monitoring-System/{{ page.repository-name }}){:target="_blank"}
- [Project Page](https://cepdnaclk.github.io/e17-co328-Greenhouse-Monitoring-System/{{ page.repository-name}}){:target="_blank"}
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)


[//]: # (Please refer this to learn more about Markdown syntax)
[//]: # (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
