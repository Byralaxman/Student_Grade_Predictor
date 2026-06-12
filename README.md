# Student Grade Predictor

A simple Python project that trains a linear regression model to predict a student's final grade based on study hours and attendance percentage. The trained model is saved as `grade_predictor_model.pkl`.

## Files

- `main code`: Python script that loads `student_data.csv`, trains the model, saves it, and prompts for input to predict a final grade.
- `student_data.csv`: Dataset containing `StudyHours`, `Attendance`, and `FinalGrade` columns.
- `grade_predictor_model.pkl`: Serialized trained model file.

## Requirements

- Python 3.x
- pandas
- scikit-learn
- joblib

## Setup

1. Install dependencies:

```bash
pip install pandas scikit-learn joblib
```

2. Ensure `student_data.csv` is in the project root.

## Usage

Run the script from the project directory:

```bash
python "main code"
```

Then enter:

- Study hours
- Attendance percentage

The script will print an estimated final grade.

## Notes

- Attendance should be between `0` and `100`.
- If `student_data.csv` is missing, the script will prompt for the correct file path.

## License

No license specified.
