# Fire Weather Index (FWI) Web Application

## Overview
The Fire Weather Index (FWI) web application predicts the Fire Weather Index (FWI) based on user-provided inputs, such as temperature, relative humidity, wind speed, and more. This application uses a machine learning model trained on various regression algorithms, with the best-performing Ridge Regression model selected for deployment.

---

## Features
- **Input Form**: Accepts user data for predicting the Fire Weather Index (FWI).
- **Machine Learning Model**: Ridge Regression for precise predictions.
- **Data Preprocessing**: StandardScaler for input data standardization.
- **User Interface**: User-friendly interface for entering data and viewing predictions.

---

## Tech Stack
### Backend:
- **Flask**: Web framework for backend development.
- **scikit-learn**: Used for training and deploying the ML model.
- **pickle**: Model and scaler serialization.

### Frontend:
- HTML templates with Flask for dynamic content rendering.

---

## Installation
### Prerequisites:
1. Python 3.7+
2. Flask
3. scikit-learn
4. pickle

### Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/fwi-app.git
   ```
2. Navigate to the project directory:
   ```bash
   cd fwi-app
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Ensure the `models/` directory contains:
   - `ridge.pkl` (the trained Ridge Regression model)
   - `scaler.pkl` (the trained StandardScaler)
5. Run the application:
   ```bash
   python app.py
   ```
6. Open the app in a browser at [http://localhost:5000](http://localhost:5000).

---

## Usage
### Input Fields:
- **Temperature**: The temperature at noon in Celsius.
- **RH**: Relative Humidity in percentage.
- **Ws**: Wind speed in km/h.
- **Rain**: Total rainfall in mm.
- **FFMC**: Fine Fuel Moisture Code.
- **DMC**: Duff Moisture Code.
- **ISI**: Initial Spread Index.
- **Classes**: Class of fire occurrence (1 for fire, 0 for no fire).
- **Region**: Geographic region identifier.

### Steps to Predict:
1. Enter the required input values in the form on the homepage.
2. Click the **Predict** button.
3. View the predicted FWI on the results page.

---

## Model Training
- **Dataset**: Preprocessed dataset containing features like temperature, humidity, wind speed, and more.
- **Algorithms**: Various machine learning models were trained and evaluated, including:
  - Logistic Regression
  - Random Forest
  - Support Vector Machine (SVM)
  - Ridge Regression (Best Performing Model)
- **Evaluation Metric**: The Ridge Regression model outperformed others in terms of accuracy and stability.


## Future Enhancements
1. **Add More Models**: Incorporate additional models for comparison and ensemble.
2. **Improved UI**: Enhance the interface for better user experience.
3. **API Integration**: Allow predictions via RESTful APIs.
4. **Real-Time Data**: Fetch weather data dynamically from external APIs.

---

## License
This project is licensed under the MIT License. See `LICENSE` for more details.

---

## Contact
For inquiries or contributions, please contact [your-email@example.com].

