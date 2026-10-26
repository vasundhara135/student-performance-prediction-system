# Student Performance Analytics & Prediction System

A machine learning-based web application that predicts student performance categories using academic scores and student-related information. The application also provides personalized study recommendations to help identify areas that may need improvement.

## Overview

The Student Performance Analytics & Prediction System uses a Random Forest Classifier to categorize student performance as **High, Average, or Low**. Users can enter student details and examination scores through an interactive Streamlit dashboard to receive a prediction and suggestions for improvement.

## Features

- **Performance Prediction:** Predicts a student's performance category using a trained machine learning model.
- **Interactive Dashboard:** Provides an easy-to-use interface built with Streamlit.
- **Student Information Input:** Accepts demographic and educational information through dropdown menus.
- **Exam Score Analysis:** Allows users to enter Mathematics, Reading, and Writing scores.
- **Personalized Recommendations:** Suggests study improvements based on individual scores and test preparation status.
- **Data Analysis:** Supports exploratory data analysis and model training.

## Technologies Used

- **Programming Language:** Python
- **Web Framework:** Streamlit
- **Machine Learning:** Scikit-learn, Random Forest Classifier
- **Data Processing:** Pandas
- **Data Visualization:** Matplotlib and Seaborn, if used in the analysis scripts
- **Model Storage:** Pickle
- **Development Environment:** Visual Studio Code

## Dataset

The project uses the Students Performance dataset, containing 1,000 student records.

The dataset includes the following attributes:

| Attribute | Description |
|---|---|
| Gender | Student gender |
| Race/Ethnicity | Demographic group |
| Parental Level of Education | Parents' highest education level |
| Lunch | Standard or free/reduced lunch |
| Test Preparation Course | Test preparation completion status |
| Math Score | Mathematics examination score |
| Reading Score | Reading examination score |
| Writing Score | Writing examination score |

The performance category is derived from the average of the three examination scores:

- **High:** Average score greater than or equal to 75
- **Average:** Average score greater than or equal to 50 and below 75
- **Low:** Average score below 50

Dataset source: [Kaggle – Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

## Project Structure

```text
student-performance-prediction-system/
├── dataset/
│   └── StudentsPerformance.csv
├── models/
│   ├── student_rf_model.pkl
│   └── label_encoders.pkl
├── screenshots/
├── report/
├── ppt/
├── main.py
├── app.py
├── requirements.txt
├── .gitignore
└── README.md
```

*Note: The directory and model filenames above should match the actual files in your repository.*

## Installation and Setup

### Prerequisites

- Python 3.10 or a compatible version supported by the project's dependencies
- Git
- Visual Studio Code (recommended)

### 1. Clone the Repository

```bash
git clone https://github.com/vasundhara135/student-performance-prediction-system.git
cd student-performance-prediction-system
```

### 2. Create a Virtual Environment

On Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Train the Machine Learning Model

Run the training script:

```bash
python main.py
```

This script should perform the data processing and model training implemented in the project and generate the model files required by the dashboard.

### 5. Launch the Web Application

```bash
python -m streamlit run app.py
```

Open the following address in your browser:

http://localhost:8501

## How to Use

1. Launch the Streamlit application.
2. Enter the student's information using the available dropdown menus.
3. Set the Mathematics, Reading, and Writing scores.
4. Click **Predict Student Performance**.
5. Review the predicted performance category and average score.
6. Read the study recommendations and identify subjects that may need additional attention.

## Model and Evaluation

The application uses a Random Forest Classifier to predict the performance category. Categorical variables are encoded using fitted LabelEncoder objects, and the trained model is loaded by the Streamlit application.

Model performance should be evaluated using an appropriate test dataset. Accuracy and other evaluation metrics should be reported only after verifying the actual results produced by the training and evaluation code.

## Future Enhancements

- Add visual comparisons of Mathematics, Reading, and Writing scores.
- Display model evaluation metrics and a confusion matrix.
- Improve recommendations using subject-wise performance analysis.
- Add downloadable prediction reports.
- Deploy the application to a public hosting platform.

## Limitations

- Predictions depend on the dataset and model used for training.
- The model's predictions are estimates and may not reflect every student's circumstances.
- The dataset's demographic attributes should be handled responsibly and should not be used to make consequential decisions about individual students.

## Acknowledgements

This project uses the Students Performance dataset available on Kaggle.

If this repository is based on an existing project, the original repository and its creator should be credited here.

## Author

**Vasundhara Naga Durga Addala**

- GitHub: [vasundhara135](https://github.com/vasundhara135)
- LinkedIn: [View LinkedIn Profile](https://www.linkedin.com/in/vasundhara-naga-durga-addala-83b70925a/)

---

*Developed as a machine learning and data analysis project to explore student performance prediction and interactive dashboard development.*