# Student Grade Predictor

A machine learning project that predicts a student's final grade based on study hours and attendance using linear regression.

## Overview

This project demonstrates a practical application of predictive analytics in education. It trains a linear regression model on student performance data to estimate final grades based on two key factors: study hours and attendance percentage. The trained model is persisted for reuse without requiring retraining.

## Features

- **Predictive Model**: Linear regression model trained on student performance data
- **Interactive Predictions**: User-friendly command-line interface for grade predictions
- **Data Persistence**: Pre-trained model saved as a serialized pickle file
- **Input Validation**: Validation checks for attendance range (0-100%)
- **Error Handling**: Robust error handling for invalid inputs and missing data files

## Project Structure

```
Student_Grade_Predictor/
├── main code                    # Main Python script for model training and predictions
├── student_data.csv             # Dataset with student performance data
├── grade_predictor_model.pkl    # Pre-trained serialized model
└── README.md                    # This file
```

## Requirements

- Python 3.x
- pandas
- scikit-learn
- joblib

## Installation

1. Clone or download this repository
2. Install the required dependencies:

```bash
pip install pandas scikit-learn joblib
```

3. Ensure `student_data.csv` is present in the project root directory

## Usage

Run the main script from the project directory:

```bash
python "main code"
```

The script will:
1. Load and train the model on `student_data.csv`
2. Save the trained model to `grade_predictor_model.pkl`
3. Prompt you to enter student information for prediction

When prompted, provide:
- **Study Hours**: Number of hours studied (numeric value)
- **Attendance Percentage**: Attendance rate as a percentage (0-100)

The script will output the estimated final grade.

### Example

```
-- Student Grade Prediction --
Enter study hours: 45
Enter attendance percentage: 85

Estimated Final Grade: 78.50
```

## Data Format

The `student_data.csv` file should contain three columns:

| StudyHours | Attendance | FinalGrade |
|------------|------------|-----------|
| 66         | 100        | 100       |

- **StudyHours**: Number of hours spent studying
- **Attendance**: Attendance percentage (0-100)
- **FinalGrade**: Final grade achieved by the student

## Notes

- Attendance values should be between 0 and 100
- The model is trained fresh each time the script runs
- If `student_data.csv` is not found, the script will alert you to verify the file path
- Non-numeric input will trigger an error message prompting for valid numerical values

## How It Works

1. The script loads student data from CSV
2. Features (Study Hours, Attendance) and target (Final Grade) are extracted
3. A linear regression model is trained on this data
4. The model is saved using joblib for future use
5. User input is collected and converted to the same feature format
6. The model predicts the final grade based on the input features

## Future Enhancements

- Add data validation and preprocessing
- Implement cross-validation for model performance evaluation
- Support for additional features (prior GPA, engagement score, etc.)
- Model performance metrics (R², MSE, MAE)
- Web interface for predictions
- Dataset expansion and model refinement

## License

This project is open source. No specific license is currently specified.

## Author

Byralaxman

---

**Disclaimer**: This model is intended for educational purposes. Predictions should be validated against actual performance and not used as the sole basis for academic decisions.
