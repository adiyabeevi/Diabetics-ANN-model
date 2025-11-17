
# Diabetes Progression Prediction using ANN

This project uses the Diabetes dataset from **scikit-learn** to model disease progression using an **Artificial Neural Network (ANN)**. The work includes preprocessing, exploratory analysis, baseline model building, evaluation, and model improvement experiments.

---

## Objectives
- Load and preprocess the Diabetes dataset  
- Perform EDA to understand feature behavior  
- Build a baseline ANN model using `MLPRegressor`  
- Train and evaluate the model  
- Improve performance using different architectures & hyperparameters  
- Compare results and document findings  

---

##  Project Structure
├── Diabetes_ANN.ipynb # Main notebook with all steps
├── README.md # Project documentation
└── requirements.txt # Dependencies

Technologies Used
- Python  
- Scikit-learn  
- Pandas  
- NumPy  
- Matplotlib  

---

## Steps Performed

### **1. Data Loading & Preprocessing**
- Loaded dataset using `load_diabetes()`
- Checked missing values (there were none)
- Normalized features using **StandardScaler**

### **2. Exploratory Data Analysis**
- Plotted target distribution
- Computed correlations
- Visualized top correlated features vs target

### **3. Building the ANN Model**
- Baseline ANN:
  - Hidden layer: `(100,)`
  - Activation: **ReLU**
  - Optimizer: **Adam**
  - Loss: **MSE (default for regression)**

### **4. Training the Model**
- 80/20 train-test split
- Model trained on scaled data

### **5. Model Evaluation**
Metrics reported:
- **Mean Squared Error (MSE)**
- **R² Score**

### **6. Improving the Model**
Two experiments were run:

**Experiment A**
- Architecture: `(50, 25)`
- Activation: ReLU
- Added regularization: `alpha = 0.001`
- Result: Slight improvement

**Experiment B**
- Architecture: `(100, 50)`
- Activation: `tanh`
- Solver: `lbfgs`
- Result: Worse performance (solver + activation mismatch)

### **7. Comparison Table**
All three models (baseline, exp A, exp B) were compared using MSE & R².

---

## Summary of Results (Example)
| Model | MSE | R² Score |
|-------|------|-----------|
| Baseline | ~3036 | ~0.42 |
| Experiment A | Slightly better | Slightly higher |
| Experiment B | Worse | Lower |
