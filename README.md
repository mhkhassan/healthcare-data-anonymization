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
## 📁 healthcare-data-anonymization  
 ┣ 📂 data  
 ┃ ┗ 📄 healthcare_dataset.csv  
 ┣ 📂 src  
 ┃ ┗ 📄 data_anonymizer.py  
 ┣ 📂 output  
 ┣ 📄 README.md  
 ┣ 📄 requirements.txt  
 ┗ 📄 .gitignore  

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

---
## ⚙️ Parameters  
You can modify these in the scripts:
- epsilon_param : Controls differential privacy noise (default 0.1)
- k_param : Minimum group size for k-anonymity (default 5)
- anonymization _strategy : 'suppression', 'generalization', or 'synthetic'

---
## 📊 Dataset
The included `healthcare_dataset.csv` is a sample dataset used for demonstration purposes.
It contains both numerical and categorical attributes suitable for anonymization techniques.

You can replace it with any structured CSV file containing similar data types.

---
## 📝 License
This project is released under the MIT License.