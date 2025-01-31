# **Bayesian Data Analysis**

## 📌 Overview  
This project explores the application of **Bayesian Logistic Regression** to analyze the progression of **liver cirrhosis**, a chronic liver disease. Using a dataset from **Kaggle**, the study examines how **clinical, demographic, and laboratory factors** influence survival outcomes. The analysis applies **Bayesian statistical methods** to enhance model interpretability and quantify uncertainty in predictions.

## 🛠️ Features  
- **Real-World Dataset**: Analyzed the "Cirrhosis Patient Survival Prediction" dataset with **418 observations** and **17 clinical attributes**.  
- **Bayesian Logistic Regression Models**: Implemented **three models** with different **prior specifications** and group-level effects.  
- **Data Preprocessing & Feature Engineering**: Performed **one-hot encoding, standardization**, and created new features using **domain knowledge**.  
- **Exploratory & Statistical Analysis**: Used **violin plots, correlation matrices**, and **posterior inference** for better insights.  
- **Model Evaluation & Comparison**: Applied **Leave-One-Out Cross-Validation (LOO-CV)** to assess model accuracy and generalizability.  
- **Sensitivity & Specificity Analysis**: Evaluated model performance using **true positive and true negative rates**.  
- **Synthetic Data Generation**: Augmented dataset size using **synthetic data** to improve model robustness.  
- **Comprehensive Diagnostics**: Conducted **MCMC trace plots, convergence checks, and posterior sampling** for model validation.  

## 📊 Methodology  
### 1️⃣ **Data Collection & Preprocessing**  
- Loaded the **cirrhosis dataset** from Kaggle and **handled missing values**.  
- Engineered new features such as **liver function index, symptom score, and age groups**.  
- Standardized numerical variables and applied **one-hot encoding** for categorical variables.  
- Generated **synthetic data** (5,000 samples) to mitigate **class imbalance**.  

### 2️⃣ **Bayesian Logistic Regression Models**  
- **Model 1**: Included **random effects for Age Group, Stage, and Symptom Score** with informative priors.  
- **Model 2**: Used **non-informative priors** and adjusted hyperparameters for model flexibility.  
- **Model 3**: Excluded **group-level effects**, focusing on fixed effects only.  
- Applied **Markov Chain Monte Carlo (MCMC)** sampling with **NUTS (No-U-Turn Sampler)**.  

### 3️⃣ **Model Comparison & Diagnostics**  
- Used **Leave-One-Out Cross-Validation (LOO-CV)** for predictive performance comparison.  
- Evaluated **sensitivity, specificity**, and **predictive accuracy** on test data.  
- Analyzed **MCMC trace plots, convergence metrics (Rhat), and effective sample size (ESS)**.  

## 📦 Dependencies  
- **R version 4.3.2**  
- `brms` – Bayesian Regression Models  
- `loo` – Leave-One-Out Cross-Validation  
- `tidyverse` – Data manipulation & visualization  
- `bayesplot` – Posterior visualization  
- `synthpop` – Synthetic data generation  

## 🚀 Results & Insights  
- **Age, bilirubin, platelets, and alkaline phosphatase levels** significantly impact survival.  
- **Model 2 (with non-informative priors) showed the best predictive performance**, followed by Model 3 and Model 1.  
- **Bayesian inference captured uncertainty** better than traditional logistic regression.  
- **Sensitivity & specificity trade-off** exists between models, impacting medical diagnosis accuracy.  
- **Synthetic data improved model robustness**, mitigating data limitations.  

## 🔍 Key Takeaways  
- **Bayesian logistic regression** provides **probabilistic insights** for clinical decision-making.  
- **Model selection depends on prior knowledge and complexity** – simpler models may generalize better.  
- **Data augmentation techniques (synthetic data) enhance model training** in small datasets.  
- **LOO-CV is effective for Bayesian model validation**, ensuring predictive reliability.  


## 📜 Authors  
- **Montasir Hasan Chowdhury**  
- **Md Emon Parvez**  
- **Mohaiminul Islam**  
(Project under **TU Dortmund**, supervised by **Prof. Dr. Katja Ickstadt & Prof. Dr. Paul Bürkner**)  

## 📌 Citation  
If you use this project, please cite:  
*"Liver Cirrhosis Bayesian Data Analysis – TU Dortmund, March 2024."*  
