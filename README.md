# Social Media and Mental Health Risk App

An end-to-end data science and machine learning project that analyzes the relationship between social media habits, digital behavior, sleep patterns, social interactions, and mental health indicators.

The repository includes multi-dataset analysis, data merging, preprocessing, feature selection, model development, evaluation visualizations, and an interactive Streamlit application called **MindTrace AI**.

> **Disclaimer:** This project was developed for educational and portfolio purposes. It is not a medical diagnosis tool and must not replace professional mental health advice.

## Project Overview

The project examines how social media and digital behavior may relate to mental health risk.

The analysis covers factors such as:

- Age and gender
- Relationship status
- Education level
- Main social media platform
- Daily screen time
- Notification frequency
- Application-switching behavior
- Sleep duration
- Effects on work or education
- Social conflicts related to digital usage

Multiple datasets were analyzed, cleaned, combined, and transformed into a model-ready structure.

## Main Features

- Analysis of multiple social media and mental health datasets
- Dataset merging and enrichment
- Missing-value and outlier handling
- Feature selection and preprocessing
- Classification model development
- Model comparison and evaluation
- Confusion matrix and ROC curve visualizations
- Learning curve and overfitting analysis
- Saved model and scaler for reusable inference
- Interactive Streamlit application
- Turkish-language user interface

## MindTrace AI Application

The Streamlit application uses 11 user-provided factors to estimate a presentation-oriented mental health risk category.

### Application Inputs

- Gender
- Age
- Relationship status
- Education level
- Main social media platform
- Daily screen time
- Daily notification count
- Daily application-switching count
- Sleep duration
- Impact on work or education
- Social conflict status

### Application Output

The application displays one of three risk categories:

- Low risk
- Moderate risk
- High risk

These outputs are model-based and intended only for educational presentation. They are not clinical assessments or validated diagnostic thresholds.

## Machine Learning Workflow

1. Analyze the source datasets independently
2. Select relevant variables
3. Merge and enrich the datasets
4. Clean and preprocess the combined data
5. Encode categorical features
6. Scale numerical variables
7. Train and compare classification models
8. Evaluate performance with confusion matrices and ROC curves
9. Analyze learning behavior and possible overfitting
10. Save the selected model and scaler
11. Load the saved artifacts in the Streamlit application

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Streamlit
- Joblib
- Plotly
- Matplotlib
- Seaborn
- Jupyter Notebook

## Repository Structure

```text
social-media-mental-health-risk-app/
├── data/
│   ├── final_merged_data.csv
│   ├── final_merged_data_fixed.csv
│   ├── mental_health_social_media_dataset.csv
│   ├── model_ready_data.csv
│   ├── processed_data.csv
│   └── social_media_data.csv
├── images/
│   ├── confusion matrices
│   ├── correlation visualizations
│   ├── ROC curve
│   └── learning curve
├── models/
│   ├── best_model.pkl
│   └── scaler.pkl
├── notebooks/
│   ├── 01_dataset_analysis_and_feature_selection.ipynb
│   ├── 02_data_merging_and_enrichment.ipynb
│   ├── 03_data_preprocessing.ipynb
│   ├── 04_model_training_and_evaluation.ipynb
│   └── 05_overfitting_and_validation_analysis.ipynb
├── app.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/betul-bostan/social-media-mental-health-risk-app.git
cd social-media-mental-health-risk-app
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on macOS or Linux:

```bash
source .venv/bin/activate
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Running the Application

Run the Streamlit application:

```bash
streamlit run app.py
```

The application will open in your web browser.

## Model Artifacts

The application loads:

- `models/best_model.pkl`
- `models/scaler.pkl`

The scaler processes the numerical input variables, while the trained classification model produces the predicted risk category.

## Visual Outputs

The `images/` directory contains:

- Correlation heatmaps
- Score distributions
- Platform and usage visualizations
- Confusion matrices
- ROC curve
- Learning curve
- Prediction distribution plots

These outputs document the analysis and model-evaluation workflow.

## Data Notes

The repository currently contains both source, intermediate, and model-ready datasets.

Future improvements should:

- Clearly document the original source of each dataset
- Add dataset licenses
- Separate raw, interim, processed, and model-ready data into subfolders
- Remove redundant intermediate files where possible
- Keep only sample data if the original datasets are large

## Limitations

- The model output should not be interpreted as a clinical diagnosis.
- Results may reflect limitations and biases in the original datasets.
- Categorical mappings in the application must remain consistent with the mappings used during model training.
- The displayed risk score is designed for presentation and does not represent a medically validated probability.
- The project currently relies on manually maintained preprocessing mappings in the Streamlit application.

## Future Improvements

- Add verified model-performance metrics to the README
- Add the selected model name and comparison table
- Refactor preprocessing into a reusable Scikit-learn Pipeline
- Save encoders together with the model
- Add automated tests
- Add model explainability with SHAP
- Deploy the Streamlit application
- Add screenshots of MindTrace AI
- Add dataset sources and licenses
- Validate the risk categories with domain expertise

## Author

**Betül Bostan**

- [GitHub](https://github.com/betul-bostan)
- [LinkedIn](https://www.linkedin.com/in/bet%C3%BCl-bostan-2105942b2/)
