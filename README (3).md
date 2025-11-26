# 🏭 Industrial Copper Modeling -- Price & Status Prediction App

## 📌 Project Overview

This project is a Streamlit-based application designed to **predict
copper selling prices** and **predict deal status (Won/Lost)** using
machine learning models trained on industrial copper transaction data.\
The app performs preprocessing, encoding, scaling, and prediction using
saved `.pkl` models.

------------------------------------------------------------------------

# 🔥 8 Key Points (With Explanation)

### **1️⃣ Dual Prediction Modes**

The application contains **two tabs**: - **Predict Selling Price** -- ML
regression model predicts copper selling price.\
- **Predict Status** -- Classification model predicts whether a deal is
**Won** or **Lost**.\
This allows users to estimate both business outcome and pricing.

------------------------------------------------------------------------

### **2️⃣ Input Validation System**

All numeric fields are validated using regex: - Prevents invalid
characters\
- Rejects empty or blank inputs\
- Ensures only numeric or decimal values are allowed\
This prevents incorrect or messy data from reaching the ML model.

------------------------------------------------------------------------

### **3️⃣ Preprocessing With Scaling & Encoding**

The app loads several preprocessing components: - **StandardScaler** for
numerical scaling\
- **OneHotEncoder / Binarizer** for categorical encoding\
- **Log transformations** for skewed numerical features\
These ensure new inputs match the model training environment.

------------------------------------------------------------------------

### **4️⃣ Flexible Dropdown-Based Inputs**

User-friendly dropdowns are provided for: - Status\
- Item Type\
- Country\
- Application\
- Product Reference\
Values are taken from the actual dataset, ensuring consistency and
preventing invalid selections.

------------------------------------------------------------------------

### **5️⃣ Selling Price Prediction**

For price prediction: - Inputs undergo log transformation\
- Features are combined with encoded variables\
- Processed through a trained regression model (`model.pkl`)\
- Output is returned as the exponential of the predicted log price\
Produces accurate and realistic market-aligned price estimates.

------------------------------------------------------------------------

### **6️⃣ Deal Status Prediction (Won/Lost)**

For status prediction: - Uses a dedicated classification model
(`cmodel.pkl`)\
- Includes selling price, customer details, product info, and physical
dimensions\
- Output: - 🟢 **Won** - 🔴 **Lost**\
Helps sales teams estimate the likelihood of securing deals.

------------------------------------------------------------------------

### **7️⃣ Pretrained Model Integration**

The app loads multiple `.pkl` files for end-to-end preprocessing and
prediction:\
- `model.pkl`, `scaler.pkl`, `t.pkl`, `s.pkl` for price prediction\
- `cmodel.pkl`, `cscaler.pkl`, `ct.pkl` for status prediction\
This ensures predictions closely match the original modeling workflow.

------------------------------------------------------------------------

### **8️⃣ Professional UI Built With Streamlit**

Features include: - Wide-page layout\
- Custom-styled buttons\
- Tab-based navigation\
- Notes for minimum/maximum field ranges\
- Clean column-based input layout\
Creates a smooth and professional experience for end users.

------------------------------------------------------------------------

# 📁 Project Structure

    📦 Industrial-Copper-Modeling/
    ├── dsindustrialcopper.py
    ├── model.pkl
    ├── scaler.pkl
    ├── t.pkl
    ├── s.pkl
    ├── cmodel.pkl
    ├── cscaler.pkl
    ├── ct.pkl
    └── README.md

------------------------------------------------------------------------

# 🧠 Future Scope

-   Add interactive EDA section\
-   Deploy the application on Streamlit Cloud\
-   Introduce advanced ML models\
-   Add selling price & status visual analytics
