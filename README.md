# 🏠 House Price Prediction with Linear Regression

> Predicting California median house values using interpretable machine learning — a clean baseline study in regression modelling, feature scaling, and coefficient analysis.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange?style=flat&logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## 📌 Project Overview

Housing markets are influenced by dozens of socioeconomic and geographic factors, making price prediction a classic and high-impact regression problem. This project builds a **Linear Regression model** on the California Housing dataset to predict median house values based on features such as income, location, and housing demographics.

The goal is not just prediction — but **interpretability**: understanding *which features drive prices* and *by how much*, making this a realistic baseline study before advancing to ensemble methods.

---

## ✨ Features

- 📊 **Exploratory Data Analysis** — statistical summary and correlation heatmap
- 🧹 **Data Preprocessing** — missing value checks, feature/target separation
- ⚖️ **Feature Standardisation** — StandardScaler applied for optimal linear model performance
- ✂️ **Train/Test Split** — 80/20 stratified split with fixed random seed for reproducibility
- 🤖 **Linear Regression Training** — scikit-learn implementation with full fit
- 🔍 **Coefficient Interpretation** — ranked bar chart showing feature impact direction and magnitude
- 📈 **Model Evaluation** — R², MSE, and RMSE metrics with clear reporting
- 🎯 **Visualisations** — Actual vs Predicted plot + Residuals diagnostic plot

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.10+ |
| Data Manipulation | pandas, NumPy |
| Machine Learning | scikit-learn |
| Visualisation | matplotlib, seaborn |
| Environment | Jupyter Notebook / VS Code |
| Dataset | California Housing (sklearn built-in) |

---

## 📸 Screenshots

### Correlation Heatmap
<img width="934" height="590" alt="output" src="https://github.com/user-attachments/assets/1d327c8c-aa7d-46cf-b051-5e947c5fc58a" />
> Feature correlation matrix — MedInc shows the strongest positive correlation with house value.

### Feature Coefficients
<img width="889" height="490" alt="2" src="https://github.com/user-attachments/assets/1f2944dd-fee4-4fad-b767-61ce896c1d15" />
> Ranked bar chart of Linear Regression coefficients — blue = positive impact, red = negative impact.

### Actual vs Predicted
<img width="790" height="590" alt="3" src="https://github.com/user-attachments/assets/04f58355-479e-4d7f-bb2d-238523bfc149" />
> Scatter plot comparing model predictions to ground truth values. The red dashed line represents perfect prediction.

### Residuals Plot
<img width="789" height="490" alt="4" src="https://github.com/user-attachments/assets/881b2ee2-8a3e-4f34-b5a1-1667d7547ded" />
> Residuals scattered around zero — indicates no severe systematic bias in predictions.

---

## ⚙️ Installation

### Prerequisites
- Python 3.10+
- pip

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/fsafva13-coder/house-price-linear-regression.git
cd house-price-linear-regression

# 2. (Optional) Create a virtual environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch the notebook
jupyter notebook linear_regression_task2.ipynb
```

> **VS Code users:** Open the `.ipynb` file directly in VS Code with the Jupyter extension installed.

---

## 🚀 Usage

1. Open `linear_regression_task2.ipynb`
2. Run all cells sequentially (`Run All` or `Shift + Enter`)
3. The notebook will:
   - Load the California Housing dataset automatically (no download needed)
   - Preprocess and scale features
   - Train the Linear Regression model
   - Print evaluation metrics to output
   - Display all 4 visualisations inline

**Expected output:**
```
R² Score : 0.5758
MSE      : 0.5559
RMSE     : 0.7456

The model explains 57.6% of the variance in house prices.
```

---

## 📁 Project Structure

```
house-price-linear-regression/
│
├── linear_regression_task2.ipynb   # Main notebook (EDA → Training → Evaluation)
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation
│
└── screenshots/                    # Visualisation outputs
    ├── correlation_heatmap.png
    ├── feature_coefficients.png
    ├── actual_vs_predicted.png
    └── residuals_plot.png
```

---

## 📊 Results & Performance

| Metric | Value |
|--------|-------|
| **R² Score** | 0.5758 |
| **Mean Squared Error (MSE)** | 0.5559 |
| **Root Mean Squared Error (RMSE)** | 0.7456 |

**Key Findings:**

- 🏆 **MedInc** (median income) is the strongest predictor — districts with higher income levels have significantly higher house prices
- 📍 **Latitude** carries a strong negative coefficient — reflecting California's geography where northern/inland areas are generally cheaper
- 🏢 **AveRooms** has a modest positive effect, while **AveOccup** (overcrowding) negatively impacts value
- The model explains ~58% of price variance — a solid interpretable baseline; ensemble models would improve this further

---

## 🧩 Challenges & Learnings

- **Feature scaling matters** — running Linear Regression without StandardScaler produced unbalanced coefficients due to different feature magnitudes; scaling made the model both more stable and more interpretable
- **Residual analysis** revealed slight heteroscedasticity at higher predicted values — a sign that linear assumptions break down for luxury-priced properties, motivating the use of non-linear models
- **Coefficient interpretation** requires caution with correlated features (e.g. Latitude/Longitude are geographically linked) — multicollinearity can inflate or suppress individual coefficients

---

## 🔮 Future Improvements

- [ ] Add **Ridge and Lasso Regression** for regularisation comparison
- [ ] Implement **Polynomial Features** to capture non-linear relationships
- [ ] Try **Random Forest / XGBoost** for significant R² improvement
- [ ] Add **cross-validation** (K-Fold) for more robust performance estimates
- [ ] Deploy as a simple **Streamlit web app** for interactive price prediction
- [ ] Incorporate **SHAP values** for model-agnostic feature importance analysis

---

## 🔗 Demo / Live Link

> 📓 Notebook available in this repository — clone and run locally.  
> 🚀 Streamlit deployment: *coming soon*

---

## 👩‍💻 Author

**Fathima Safva**  
BSc Computer Science | University of West London (UAE Campus)  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://linkedin.com/in/fathima-safva-578294315)
[![GitHub](https://img.shields.io/badge/GitHub-fsafva13--coder-black?style=flat&logo=github)](https://github.com/fsafva13-coder)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

*Built as part of the Codveda Technologies Machine Learning Internship — Level 1, Task 2.*
