# 🏨 Hotel Bookings Data Cleaning & Exploration

## 📌 Project Description
This project explores and cleans the **Hotel Bookings Dataset** to handle missing values, fix outliers, and visualize key booking patterns.  
It demonstrates data preprocessing, feature handling, and exploratory data analysis (EDA) — essential steps before building machine learning models.

---

## 📂 Dataset
The dataset used is **hotel_bookings.csv**, which contains information about hotel reservations including booking details, guest demographics, and reservation outcomes.

---

## 🛠 Steps Performed

### 🔹 1. Dataset Understanding
- Created a **Markdown table** describing all columns and their meaning.  
- Understood the type of each feature (categorical, numerical, datetime).

### 🔹 2. Data Cleaning
- Removed invalid values in **`is_canceled`** (kept only `0` and `1`).  
- Dropped **duplicates** (~4000 rows).  
- Handled missing values:  
  - **company** → replaced with `"Unknown"` (since it’s just an ID).  
  - **agent** → replaced with `0` (missing agent ID).  
  - **children** → replaced with `0` (logical since most values are 0).  
  - **country** → replaced with `"Unknown"`.  
- Fixed invalid/strange values:  
  - **adr**: converted negative values → absolute.  
  - Removed extreme **outliers** in `adr` using **IQR method**.  
  - Replaced zero values in `adr` with **median**.  
  - **lead_time**: removed unrealistic values (> 365 days).  

### 🔹 3. Data Visualization
Created a **dashboard-like section** to explore booking patterns:
- Distribution of **ADR** and **Lead Time**.  
- **Hotel type counts** (City vs Resort).  
- ADR distribution by **Hotel**, **Customer Type**, **Deposit Type**.  
- Relationship between **ADR** and **Cancellation**.  
- **Monthly ADR trend** (seasonality).  
- **Correlation Heatmap** for numerical features.

### 🔹 4. Encoding
- Applied **Label Encoding** for categorical columns to prepare the dataset for future modeling.

---

## 📊 Example Visualizations
- **ADR Distribution**  
- **Hotel Type vs ADR**  
- **ADR by Deposit Type**  
- **Monthly ADR Trend**  
- **Correlation Heatmap**  

*(Screenshots/plots can be added here if desired)*

---

## 🚀 Tech Stack
- **Python** 🐍  
- **Pandas & NumPy** – Data manipulation  
- **Matplotlib & Seaborn** – Visualization  
- **Scikit-learn** – Preprocessing & Encoding  

---

## 📁 Repository Structure
