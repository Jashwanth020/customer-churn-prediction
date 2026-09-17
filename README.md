# Customer Churn Prediction

This project builds a predictive machine learning pipeline to identify customers at risk of churning. Using Artificial Neural Networks (ANN) and traditional machine learning algorithms, the system evaluates customer demographics and financial behavior to output a churn probability score.

## Features
- **Data Preprocessing**: Handles missing data, categorical encoding (Label Encoding, One-Hot Encoding), and feature scaling.
- **Deep Learning Model**: A custom ANN built with TensorFlow/Keras to model complex non-linear relationships.
- **Traditional ML Models**: Benchmarking with standard machine learning algorithms.
- **Web Application**: Interactive web deployment to evaluate real-time customer data.

## Project Structure
- \pp.py\: The web application file for the deployment interface.
- \Customer_Churn_Prediction_ANN.ipynb\: Jupyter notebook detailing the data exploration, preprocessing, and building of the ANN model.
- \Customer_Churn_Prediction_ML_Algos.ipynb\: Notebook exploring baseline machine learning models.
- \hyperparametertuningann.ipynb\: Notebook covering hyperparameter tuning for the ANN.
- \prediction.ipynb\: Demonstration of making predictions with the trained models.
- equirements.txt\: Python environment dependencies.
- \*.pkl\ & \*.h5\: Serialized models, scalers, and encoders used for inference.

## Getting Started

### Prerequisites
Ensure you have Python installed.

### Installation
1. Clone this repository:
   \\ash
   git clone https://github.com/Jashwanth020/customer-churn-prediction.git
   cd customer-churn-prediction
   \\n2. Create and activate a virtual environment (optional but recommended):
   \\ash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   \\n3. Install the dependencies:
   \\ash
   pip install -r requirements.txt
   \\n
### Running the Application
Start the web application using the following command (Streamlit application):
\\ash
streamlit run app.py
\\n