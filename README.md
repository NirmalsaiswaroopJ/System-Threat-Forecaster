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
- **Visualizations/**: A folder to store any generated plots or visualizations.
- **LICENSE**: License file detailing the terms for project usage.
- **Machine Learning Practice Consolidated Notes.pdf**: Contains notes and learning material related to machine learning.
- **Notebook-CodeWork.ipynb**: The main Jupyter notebook where the model development and analysis are carried out.
- **README.md**: The documentation file providing an overview of the project and setup instructions.
- **System-Threat-Forecaster.zip**: A compressed file that includes project files for easy sharing.
- **sample_submission.csv**: The sample CSV file used for competition submission with the required format.
- **requirements.txt**: Consists of all the dependencies that need to be pre-installed.

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
### Procedure

```bash
# Run the notebook to reproduce results
jupyter notebook Notebook-CodeWork.ipynb
```
### Submission

Submit the results
After generating the predictions, submit the final output file (submission.csv) to the competition or project platform.

## Results and Findings

Our LightGBM model identified the following critical factors in malware prediction:

- **Signature update recency** (27% importance)
- **Real-time protection state** (21% importance)
- **OS version** (18% importance)
- **RAM capacity** (9% importance)

These findings suggest that security posture management and regular updates are the most effective preventative measures against malware infection.

## 🔮 Future Work

I've identified several promising directions for future research:

- Incorporation of temporal features to capture infection patterns over time
- Ensemble approach combining multiple model strengths
- Deep learning approaches for feature extraction from raw telemetry data
- Explainability enhancements for security operations teams

## 👥 Contributors

- **Nirmal Sai Swaroop J** - Learning Data Science Student
- **IIT Madras Data Science Program** - Academic Support

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- IIT Madras for the excellent Data Science curriculum
- Open-source ML libraries that made this analysis possible

## 🌐 Connect with Me

- LinkedIn: [Profile](https://www.linkedin.com/in/nirmal-sai-swaroop-janapaneedi-4aa5632a7/)

## 💬 Thank You!

