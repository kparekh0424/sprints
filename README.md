# sprints

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

##  Project Description

This project investigates how machine learning models can improve the accuracy of hyperlocal weather forecasts by predicting the difference between forecasted and actual temperatures. It uses real-time weather data from the National Weather Service (NWS) and NOAA's METAR API to build a data pipeline that includes data collection, cleaning, feature engineering, model training, and evaluation.

The project uses Ridge Regression and Random Forest Regressor to compare modeling approaches for predicting temperature error. These models are trained on processed data with engineered features like lag values, rolling averages, and wind speed bins. The ultimate goal is to produce a scalable system that helps improve location-specific weather predictions, enabling better planning for individuals, businesses, and public services.

## Dependencies

Ensure you're using Python 3.10 or higher. Install dependencies with:

```bash
pip install -r requirements.txt
```
Key libraries used:
- pandas
- numpy
- scikit-learn
- matplotlib
- requests
- datetime
- jupyter notebook

## 🧪 Setting Up the Environment

1. Clone the repository:
```bash
git clone https://github.com/your-username/sprints_inst414_project.git
cd sprints
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 🔄 Running the Data Processing Pipeline

Open the Jupyter notebook:

```bash
jupyter notebook notebooks/sprints2.ipynb
```

The notebook performs the following:
- Pulls forecast and actual temperature data using the NWS and METAR APIs
- Merges datasets by timestamp
- Cleans missing values and removes outliers
- Creates engineered features (e.g., lag variables, rolling means, wind categories)
- Trains and evaluates two machine learning models

Processed datasets will be saved in `data/processed/`.

## 📊 Evaluating Models

Two models are trained and evaluated:
- Ridge Regression
- Random Forest Regressor

Evaluation metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score
- 5-Fold Cross-Validation

Visualizations (histograms, scatter plots, feature importances) are displayed within the notebook.

## Reproducing Results

To reproduce the results:
1. Set up your environment and install dependencies
2. Run the notebook from top to bottom
3. Optionally, modularize steps into scripts 

The project follows the [Cookiecutter Data Science](https://cookiecutter-data-science.drivendata.org/) structure for maximum reproducibility and collaboration.

## Project Structure

```
├── data copy/
│   ├── raw/               <- Original weather data from APIs
│   └── processed/         <- Cleaned and merged data used for modeling
├── notebooks/             <- Jupyter notebooks for data processing and model training
├── inst_414/              <- Source code (scripts for data and model functions)
├── models/                <- Trained model files 
├── reports/
    ├── figures/           <- Visualizations: generated plots and charts
├── references/            <- Data dictionaries, API docs, external sources
├── requirements.txt       <- Python dependencies
├── README.md              <- This file
```

## License
This project does not include an open-source license at this time.

## Author
Kavita Parekh 
University of Maryland, INST 414  
Spring 2025
