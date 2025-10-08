# DSAS5205 Project 1 – The Virtue of Complexity in Return Prediction

**Name:** Jianing Li  
**Student ID:** A0330643M  
**Email:** E1561405@u.nus.edu

---

## 1. Project Overview

This project reproduces and extends the results of *Kelly, Malamud, and Zhu (2024)*,  
“The Virtue of Complexity in Return Prediction.”

It includes three main components:

- **Task 1:** Simulate misspecified Ridge regression to verify the “virtue of complexity.”  
- **Task 2:** Extend the simulation to Lasso regression for comparison.  
- **Task 3:** Apply the methods to three real-world financial datasets (A, B, C),  
  performing model selection and prediction.

The goal is to demonstrate how model complexity and regularization interact  
to optimize out-of-sample performance.

## 2. Environment Setup

**Python version:** 3.13  
Install dependencies with:

pip install -r requirements.txt

All random seeds are fixed for reproducibility:
np.random.seed(12345)
random.seed(12345)

## 3. Folder Structure

The repository is organized as follows:

- **Code/** – contains all Jupyter notebooks for simulation and empirical analysis  
  - `Task1.ipynb`: finite-sample simulation for misspecified Ridge regression  
  - `Task1_Largesample.ipynb`: large-sample version for asymptotic behavior  
  - `Task2.ipynb`: extension to Lasso regression  
  - `Task3A.ipynb`, `Task3B.ipynb`, `Task3C.ipynb`: analyses and model selection for datasets A, B, C  
- **Data/Input/** – includes all provided training and test feature files (`pairA_train.csv`, etc.)  
- **Data/Output/** – automatically stores generated prediction CSVs for Task 3  
- **Graph/** – manually saved figures produced during EDA and model comparison  
- **Report/** – final project report in PDF format  
- **Paper/** – the reference paper (*Kelly, Malamud, and Zhu, 2024*)  
- **requirements.txt** – list of Python packages required to reproduce results  
- **README.md** – project documentation and run instructions

## 4. Expected Outputs

- Simulation plots (Task 1 & 2) manually saved under `Graph/`  
- Prediction files automatically saved under `Data/Output/`:
  - `A0330643M_predictions_A.csv`
  - `A0330643M_predictions_B.csv`
  - `A0330643M_predictions_C.csv`
- Each notebook prints:
  - Progress logs showing execution steps  
  - Best parameters and corresponding Sharpe Ratios  
  - Confirmation messages for saved prediction files


## 5. How to Run

Run each notebook in order using Jupyter.  
All paths are relative, and outputs are saved automatically in `Data/Output/`.

```bash
# Task 1 – Ridge simulation
jupyter nbconvert --execute --inplace Code/Task1.ipynb
jupyter nbconvert --execute --inplace Code/Task1_Largesample.ipynb

# Task 2 – Lasso extension
jupyter nbconvert --execute --inplace Code/Task2.ipynb

# Task 3 – Datasets A, B, C
jupyter nbconvert --execute --inplace Code/Task3A.ipynb
jupyter nbconvert --execute --inplace Code/Task3B.ipynb
jupyter nbconvert --execute --inplace Code/Task3C.ipynb

