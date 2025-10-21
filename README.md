# 🛡️ Healthcare Data Anonymization
This project demonstrates practical **data anonymization techniques** applied to a **sample healthcare dataset** using Python.  
It applies **differential privacy** to numerical columns and **k-anonymity** strategies to categorical columns, helping protect sensitive information while retaining data utility.

---
## 📌 Objectives
- Apply **Differential Privacy** for anonymizing numerical attributes by adding Laplace noise.
- Implement **K-Anonymity** strategies — suppression, generalization, and synthetic replacement — for categorical attributes.
- Generate an anonymized dataset that preserves privacy while allowing further analysis.

---
## 🧠 Techniques Implemented

### 🔸 Differential Privacy
- Identifies numeric columns and calculates sensitivity (max - min).  
- Adds Laplace noise based on a configurable **epsilon (ε)** parameter.  
- Lower ε ⇒ stronger privacy but more noise.

---
### 🔸 K-Anonymity
For string columns, supports:
- **Suppression**: Replaces rare values (below `k`) with `NaN`.  
- **Generalization**: Truncates values to reduce uniqueness.  
- **Synthetic Replacement**: Replaces values with randomly selected synthetic ones from existing categories.

---
## 🗂️ Project Structure  
├─ data/  
│ └─ healthcare_dataset.csv # Input dataset  
├─ src/  
│ └─ data_anonymizer.py # Main anonymization script  
├─ output/  
│ └─ anonymized_dataset.csv # Generated output after running script  
├─ README.md  
└─ requirements.txt  

---
## 🚀 How to Run
1. **Install dependencies**
   ```bash
   pip install -r requirements.txt

2. **Run the script**
    ```bash
    python src/data_anonymizer.py

3. **Check output**
    ```bash
    output/anonymized_dataset.csv


