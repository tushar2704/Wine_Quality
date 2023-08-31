# Wine Quality Prediction with MLFLOW experiments 
### Predicting wine quality using machine learning techniques and managing the end-to-end workflow with MLFLOW experiments on Dagshub, Deployment via Docker image on AWS EC2
![Python Version](https://img.shields.io/badge/python-3.11%20%7C%203.10-blue)
![MLflow Version](https://img.shields.io/badge/MLflow-2.6.0-green)



  - [Data Preparation](#data-preparation)
  - [Training](#training)
  - [Prediction](#prediction)
- [Project Structure](#project-structure)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project aims to predict the quality of wines using various machine learning algorithms. It utilizes the MLflow platform to manage the end-to-end machine learning lifecycle, including data preprocessing, model training, hyperparameter tuning, and deployment.

## Features

- Data preprocessing pipeline for cleaning and transforming the dataset.
- Support for multiple machine learning algorithms for wine quality prediction.
- Hyperparameter tuning using grid search or random search.
- Tracking and logging experiments with MLflow for easy comparison.
- REST API endpoint for making predictions using the trained model.
- Dockerized environment for seamless deployment.


## Project Structure
```
├── data/
│   ├── wine-quality.csv
│   └── ...
├── models/
│   ├── model.pkl
│   └── ...
├── notebooks/
│   ├── data_exploration.ipynb
│   ├── model_experimentation.ipynb
│   └── ...
├── .gitignore
├── Dockerfile
├── preprocess_data.py
├── train.py
├── predict_api.py
└── README.md
```

## Getting Started

### STEPS:

Clone the repository

```bash
https://github.com/tushar2704/Wine_Quality
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n ml python=3.11 -y
```

```bash
conda activate ml
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```



## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/tushar27/Wine_Quality.mlflow \
MLFLOW_TRACKING_USERNAME=tushar27 \
MLFLOW_TRACKING_PASSWORD=31e97a76110fac92de36585f12fb7c9ce02ea9f20 \
python main.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/tushar27/Wine_Quality.mlfloww

export MLFLOW_TRACKING_USERNAME=tushar27 

export MLFLOW_TRACKING_PASSWORD=31e97a76110fac92de36585f12fb7c9ce02ea9f20

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.ap-south-1.amazonaws.com/mlproj

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app

## Contact Information

If you have any questions, feedback, or collaboration opportunities, please feel free to reach out to me. You can contact me via email at [info@tushar-aggarwal.com](mailto:info@tushar-aggarwal.com) or connect with me on LinkedIn at [Tushar Aggarwal](https://www.linkedin.com/in/yourname).

Thank you for visiting my Data Analysis Portfolio! I hope you find my projects informative and insightful.



## Author
- [<ins><b>©2023 Tushar Aggarwal. All rights reserved</b></ins>](https://www.tushar-aggarwal.com/)
- <b>[LinkedIn](https://www.linkedin.com/in/tusharaggarwalinseec/)</b>
- <b>[Medium](https://medium.com/@tushar_aggarwal)</b> 
- <b>[Tushar-Aggarwal.com](https://www.tushar-aggarwal.com/)</b>
- <b>[New Kaggle](https://www.kaggle.com/tagg27)</b> 













