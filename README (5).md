# Phishing Website Detection Using Machine Learning

## Project Overview
This project uses machine learning to classify URLs as legitimate or phishing websites. It uses website and URL-related features from the PhiUSIIL Phishing URL Dataset and a Support Vector Machine (SVM) model.

## Objectives
- Explore and prepare the phishing URL dataset.
- Select numerical features for model training.
- Train a Linear Support Vector Classifier (LinearSVC).
- Evaluate the model using a confusion matrix and classification metrics.

## Dataset
- **Dataset:** PhiUSIIL Phishing URL Dataset
- **Rows:** 235,795
- **Columns:** 56
- **Features used:** 50 numerical features after removing the target and selected text columns.

The dataset file used in the notebook is `PhiUSIIL_Phishing_URL_Dataset.csv`.

## Technologies and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Methodology
1. Load the dataset using Pandas.
2. Check the dataset structure and missing values.
3. Prepare the target labels and select numerical features.
4. Replace infinite values and fill missing feature values with their median.
5. Split the data into training and testing sets using an 80:20 ratio.
6. Scale the features using `StandardScaler`.
7. Train a `LinearSVC` model.
8. Evaluate predictions using a confusion matrix and other classification metrics.

## Model
The notebook uses a machine learning pipeline containing:
- `StandardScaler` for feature scaling.
- `LinearSVC` for classification.

The model is configured with `class_weight="balanced"`, `random_state=42`, and `max_iter=5000`.

## Results
The notebook's displayed confusion matrix is:

| Actual class | Predicted legitimate (0) | Predicted phishing (1) |
|---|---:|---:|
| Legitimate (0) | 26,970 | 0 |
| Phishing (1) | 0 | 20,189 |

These displayed results show that all 47,159 test samples were classified correctly in this run. Results should be verified by rerunning the notebook, and unusually perfect performance may warrant checking the dataset labels and feature leakage before drawing conclusions.

## How to Run
1. Download or clone this repository.
2. Place `PhiUSIIL_Phishing_URL_Dataset.csv` in the location expected by the notebook, or update the CSV path in the code.
3. Open `ML_Task9.ipynb` in Jupyter Notebook or Google Colab.
4. Install the required libraries if they are not already available.
5. Run the notebook cells in order.

Example installation command:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Note
This is an educational machine learning project. Its predictions should not be treated as a guarantee that a website is safe or malicious.

## Author
Sangeetha
