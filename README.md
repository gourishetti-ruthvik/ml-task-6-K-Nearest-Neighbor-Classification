# 📘 Task-6: K-Nearest Neighbour (KNN) Classification

## 🎯 Objective
Implement the K-Nearest Neighbour (KNN) classification algorithm on the Iris dataset. Tune hyperparameter `K`, evaluate model performance using metrics, and visualize decision boundaries.

---

## 📚 Dataset: Iris Dataset

- **Source**: `Iris.csv`
- **Features Used**:
  - SepalLengthCm
  - SepalWidthCm
  - PetalLengthCm
  - PetalWidthCm
- **Target**: Binary target based on PetalLengthCm
  - Class `0`: PetalLengthCm < 2.5
  - Class `1`: PetalLengthCm ≥ 2.5

---

## 🔧 Workflow Summary

### 1️⃣ Data Preprocessing
- Loaded the Iris dataset
- Checked for null values
- Dropped unnecessary columns (`Id`)
- Created a binary target variable using a lambda function
- Scaled features using `StandardScaler`

### 2️⃣ Train-Test Split
- Performed an 80-20 split of the dataset into training and testing sets

### 3️⃣ Model Training
- Used `KNeighborsClassifier` from `sklearn.neighbors`
- Trained the model on the training data

### 4️⃣ Hyperparameter Tuning
- Iterated through values of `K` from 1 to 10
- Recorded the accuracy for each `K` to observe how model performance changes

### 5️⃣ Evaluation Metrics
- Used:
  - `accuracy_score` for performance
  - `confusion_matrix` for classification analysis

### 6️⃣ Visualization
- **Decision Boundary**: Plotted using first 2 features (after scaling)
- Used `matplotlib` with `contourf` and `scatter` to visualize KNN boundaries for classification regions

---

## 📊 Results

| K Value | Accuracy |
|--------:|---------:|
| 1       | ✅ High  |
| 2–10    | 📉 Varies (trend shown in notebook) |

> Confusion matrix and accuracy shown for selected best `K`

---

## 🧰 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `sklearn` (neighbors, model_selection, metrics, preprocessing)

---

## 📌 File Structure

```bash
├── K_Nearest_Neighbour_Classification.ipynb
├── data
|    └── Iris.csv
└── README.md
