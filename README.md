# System Threat Forecaster - Malware Prediction

## Overview

This project is part of the capstone project for the IIT Madras Diploma in Data Science and Applications. The goal of this project is to predict the probability of a system being infected by various families of malware based on telemetry data collected by the system’s antivirus software. The dataset consists of machine properties and threat detection logs, which are used to build and train machine learning models that predict the likelihood of infection.

**Competition Details**:  
- **Dataset**: `train.csv`, `test.csv`  
- **Submission Format**: `id, target`  
- **Evaluation Metric**: Accuracy Score between predicted and actual values.

### Problem Statement

You are given telemetry data from a number of systems, including various attributes such as installed antivirus products, operating system details, hardware specifications, and more. The task is to predict whether each system is infected by malware based on these features.

### Dataset Description

The dataset consists of the following columns:

- **MachineID**: Unique identifier for each machine.
- **ProductName**: Name of the installed antivirus product.
- **EngineVersion**: Version of the antivirus engine.
- **AppVersion**: Version of the antivirus application.
- **SignatureVersion**: Version of the antivirus signatures.
- **IsBetaUser**: Whether the user is on a beta version of the antivirus.
- **RealTimeProtectionState**: Status of real-time protection.
- **IsPassiveModeEnabled**: Whether passive mode is enabled.
- **Other features**: Several system properties such as OS version, number of antivirus products installed, physical RAM, and more.
- **Target**: A binary indicator (0 or 1) indicating if the machine is infected by malware.

## Project Structure

The project is organized into the following structure:

SystemThreatForecaster/
│
├── Visualizations/                          # Folder for any data visualizations (if any)
│
├── LICENSE                                  # License file
│
├── Machine Learning Practice Consolidated Notes.pdf   # Practice notes PDF
│
├── Notebook-CodeWork.ipynb                  # Jupyter Notebook for model development and experimentation
│
├── README.md                                # Project documentation
│
├── System-Threat-Forecaster.zip             # Zip file containing project-related files
│
├── sample_submission.csv                   # Sample submission file for competition

## Models Implemented

The following machine learning models have been implemented to predict the target variable:

1. **Decision Tree**: The baseline model used to compare performance.
2. **Random Forest**: An ensemble model that improves upon decision trees.
3. **LightGBM**: A gradient boosting model that performs well on large datasets.
4. **Naive Bayes**: A probabilistic classifier used for comparison.
5. **Logistic Regression**: A simple linear model used for binary classification.

### Best Performing Model: LightGBM

After evaluating various models, **LightGBM** provided the best performance with an accuracy score of **0.6316**.

## How to Run the Project

### Prerequisites

Make sure you have the following libraries installed:

```bash
pip install -r requirements.txt
```
