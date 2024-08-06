# Employee Salary Predictor

The Employee Salary Predictor is a web application that estimates employee salaries based on their experience, test scores, and interview scores. Built using Flask for deployment and incorporating a linear regression model, this application provides both a web interface and API endpoint for salary predictions.

## About This Application

Accurate salary prediction is essential for various business applications, including budgeting, compensation planning, and hiring decisions. This application leverages a machine learning model trained on historical hiring data to predict employee salaries based on input features such as experience, test scores, and interview scores.

### Key Features

- **Web Interface**: Allows users to input employee details and receive salary predictions through a simple HTML form.
- **API Endpoint**: Provides an API for direct integration and predictions through HTTP requests.
- **Linear Regression Model**: Uses a trained model to predict salaries based on input features.

## Tech Stack

- **Flask**: Framework for deploying the web application and creating a user interface.
- **scikit-learn**: Library used for training the linear regression model.
- **Pickle**: Used for saving and loading the trained model.
- **Python**: Programming language used for developing both the application and the model.

## File Structure

- **app.py**: Main Flask application file handling web requests and predictions.
- **model.py**: Script for training the linear regression model and saving it using Pickle.
- **model.pkl**: Serialized model file used for predictions.
- **index.html**: HTML template for the web interface.

## Getting Started

### Prerequisites

- Python 3.x
- Flask
- scikit-learn
- Pandas
- Pickle

### Installation

1. **Clone the Repository**:
    
    ```bash
    
    git clone https://github.com/yourusername/Employee_Salary_Predictor.git
    cd Employee_Salary_Predictor
    ```
    
2. **Install Dependencies**:
    
    ```bash
    
    pip install -r requirements.txt
    ```
    
3. **Train and Save the Model**:
    - Run the `model.py` script to train the model and save it as `model.pkl`.
    
    ```bash
    
    python model.py
    ```
    

### Running the Application

1. **Start the Flask Application**:
    
    ```bash
    python app.py
    ```
    
2. **Access the Web Interface**:
    - Open a web browser and navigate to `http://127.0.0.1:5000` to interact with the application.
3. **Use the API Endpoint**:
    - **Predict Salary**:
        - **Endpoint**: `/predict_api`
        - **Method**: POST
        - **Request Format**: JSON (e.g., `{"experience": 2, "test_score": 9, "interview_score": 6}`)
        - **Response**: JSON containing the predicted salary.

### Example Usage

- **Web Interface**:
    - Enter experience, test score, and interview score in the form and submit to get the predicted salary.
- **API Request**:
    
    ```bash
    
    curl -X POST -H "Content-Type: application/json" -d '{"experience": 2, "test_score": 9, "interview_score": 6}' http://127.0.0.1:5000/predict_api
    
    ```
    

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or suggestions, please contact us at pavi2468kuk@gmail.com
