# 🛡️ Insurance Claim Severity Prediction

### **Machine Learning Project (LightGBM + SHAP + Tableau Dashboard)**

---

## 📌 **Objective**

Predict **how large an insurance claim will be (severity)** using machine learning — a critical task in:

* Pricing
* Underwriting
* Reserving
* Portfolio risk management

This project uses advanced ML techniques, explainability (SHAP), and dashboard visualization.

---

## 📂 **Project Structure**

```
insurance-claim-severity-ml-project/
│

├── Claim severity project.ipynb
│
│── lgbm_severity.pkl
│
│── severity_dashboard_data.csv
│
|── Kaggle Dataset (link in below)
│
├── requirements.txt
└── README.md
```

---

## 📊 **Dataset** 

French Motor Third-Party Liability (freMTPL2)
Dataset link (Kaggle):
**[https://www.kaggle.com/datasets/karansarpal/freMTPL2-french-motor-tpl-insurance-claims](https://www.kaggle.com/datasets/karansarpal/freMTPL2-french-motor-tpl-insurance-claims)**

Files used:

* `freMTPL2freq.csv` — policy features
* `freMTPL2sev.csv` — claim severity

---

## 🧹 **1. Data Cleaning & Preprocessing**

Steps performed:

✔ Merge frequency + severity datasets
✔ Handle missing values
✔ Convert categorical fields
✔ Feature engineering:

* `Power_x_DrivAge` (interaction)
* `DrivAge_bucket` (segmentation)

✔ Optional calculation of claim severity
✔ Export cleaned file → `processed_severity.csv`

---

## 🔍 **2. Exploratory Data Analysis (EDA)**

Includes:

* Claim severity distribution
* Correlation heatmap
* Severity by:

  * vehicle power
  * driver age bucket
  * region
* Outlier investigation

EDA provides insurance risk insights before modeling.

---

## 🤖 **3. Machine Learning Models**

### Models Trained

* Linear Regression
* Random Forest
* Gradient Boosting
* **LightGBM (best performer)**

### Metrics

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**

### Final Output

The trained LightGBM model saved as:
`models/lgbm_severity.pkl`

---

## 🧠 **4. SHAP Explainability**

Explainable AI is essential for insurance pricing and regulatory requirements.

Delivered:

* SHAP summary plot (global feature importance)
* SHAP bar plot
* SHAP contribution plots for sample predictions

This helps understand **why** a claim is predicted as severe.

---

## 📈 **5. Tableau Dashboard**

A visualization built using `severity_dashboard_data.csv`.

Includes:

* **Heatmap**: driver age bucket × vehicle power
* **Predicted vs Actual severity** scatter
* **Segment-level risk patterns**

Useful for actuarial and underwriting teams.

---

## ⚙️ **Technologies Used**

**Programming & ML**

* Python
* Pandas
* Numpy
* Scikit-learn
* LightGBM
* SHAP

**Visualization**

* Tableau
* Matplotlib / Seaborn

**Others**

* Jupyter Notebooks
* Git / GitHub

---

**How to Run (Ubuntu + Miniconda)**

### **1️⃣ Create and activate a Conda environment**

Open your terminal:

```bash
conda create -n claim_severity_env python=3.10 -y
conda activate claim_severity_env
```

---

### **2️⃣ Install project dependencies**

Use the provided `requirements.txt`:

```bash
pip install -r requirements.txt
```

(Using pip inside conda is perfectly fine.)

---

### **3️⃣ Download the Kaggle dataset**

From Kaggle:
[https://www.kaggle.com/datasets/karansarpal/freMTPL2-french-motor-tpl-insurance-claims](https://www.kaggle.com/datasets/karansarpal/freMTPL2-french-motor-tpl-insurance-claims)

Copy the following files into your project’s `data/` folder:

```
data/
├── freMTPL2freq.csv
└── freMTPL2sev.csv
```

> ⚠️ (Note) These files are not uploaded to GitHub because they are large.
> Users must download them manually.

---

### **4️⃣ Open the Jupyter notebooks**

Launch Jupyter Notebook:

```bash
jupyter notebook
```



## 🙌 **Author**

**Deepali Sharma**
Data Analyst | Machine Learning Enthusiast
https://github.com/deepalis141 • https://www.linkedin.com/in/deepali007


---

## 🏁 **Results**

This project demonstrates the full ML lifecycle:

* robust data preprocessing
* advanced ML modeling
* model interpretability
* dashboard storytelling

Ideal for actuarial, insurance, data science, and predictive analytics roles.


