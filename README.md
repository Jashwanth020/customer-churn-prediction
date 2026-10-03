# Customer Churn Prediction

A machine learning pipeline that identifies bank customers at risk of churning. It uses an Artificial Neural Network (ANN) alongside traditional ML algorithms to evaluate customer demographics and financial behavior and output a churn probability score, served through an interactive Streamlit web app.

## Dataset

The project uses the **Bank Customer Churn Prediction** dataset from Kaggle:

- **Source:** [Bank Customer Churn Prediction Dataset](https://www.kaggle.com/datasets/saurabhbadole/bank-customer-churn-prediction-dataset) by Saurabh Badole
- **Size:** 10,000 customer records
- **Target:** `Exited` (1 = customer churned, 0 = customer stayed)
- **Features:** `CreditScore`, `Geography`, `Gender`, `Age`, `Tenure`, `Balance`, `NumOfProducts`, `HasCrCard`, `IsActiveMember`, `EstimatedSalary`
- **Identifier columns** (`RowNumber`, `CustomerId`, `Surname`) carry no predictive signal and are dropped during preprocessing.

## Features

- **Data Preprocessing:** Handles missing data, categorical encoding (Label Encoding and One-Hot Encoding) and feature scaling.
- **Deep Learning Model:** A custom ANN built with TensorFlow/Keras to capture complex non-linear relationships.
- **Traditional ML Models:** Baseline benchmarking with standard machine learning algorithms.
- **Hyperparameter Tuning:** Systematic tuning of the ANN architecture and training parameters.
- **Web Application:** A Streamlit interface for scoring customer data in real time.

## Project Structure

| File | Description |
|------|-------------|
| `app.py` | Streamlit web application for deployment |
| `Customer_Churn_Prediction_ANN.ipynb` | Data exploration, preprocessing and ANN model building |
| `Customer_Churn_Prediction_ML_Algos.ipynb` | Baseline machine learning models |
| `hyperparametertuningann.ipynb` | Hyperparameter tuning for the ANN |
| `prediction.ipynb` | Making predictions with the trained model and encoders |
| `requirements.txt` | Python dependencies |
| `*.pkl`, `*.h5` | Serialized scalers, encoders and the trained model used for inference |

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Jashwanth020/customer-churn-prediction.git
   cd customer-churn-prediction
   ```

2. (Optional but recommended) Create and activate a virtual environment:

   ```bash
   python -m venv venv

   # Windows
   venv\Scripts\activate

   # macOS / Linux
   source venv/bin/activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/saurabhbadole/bank-customer-churn-prediction-dataset) and place the CSV file in the project root. This is only needed to re-run the notebooks; the web app uses the saved model files.

### Running the Application

Start the Streamlit app:

```bash
streamlit run app.py
```

Then open the local URL shown in the terminal, enter a customer's details, and the app returns their churn probability.

## Tech Stack

Python, TensorFlow/Keras, scikit-learn, pandas, NumPy, Streamlit

## Acknowledgements

Dataset by [Saurabh Badole](https://www.kaggle.com/saurabhbadole) on Kaggle.
