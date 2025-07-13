# 🍼 Newborn Weight Predictor

My first and very basic machine learning project that predicts the **birth weight of a newborn baby** based on the physical attributes and habits of the mother, such as height, weight, age, and smoking status.

---

## 🚀 Project Overview

This project uses a small dataset (≈1200 entries) sourced from Kaggle to train a regression model that estimates the weight of newborn babies. The model is trained using `scikit-learn`, served through a `Flask` backend, and deployed on [Render.com](https://render.com) with a simple HTML frontend interface.
The project is LIVE - [Predict Your Future Baby Weight](https://birth-weight-predictor-6hlb.onrender.com)

---

## 🧠 Machine Learning Pipeline

- **Dataset**: Kaggle dataset with 1200 entries including columns like:
  - `gestation`, `parity`, `age`, `height`, `weight`, `smoke`, etc.
- **Preprocessing**:
  - Split into training (80%) and testing (20%) sets
  - Checked correlation matrix to understand feature impact
- **Model Training**:
  - Used Scikit-learn regression models
  - Trained using `.fit()` and evaluated using `.predict()`
  - Model performance (e.g., R² score) is limited due to small dataset size
- **Evaluation**:
  - Predictions are generally realistic despite the small dataset size

---

## 🌐 Deployment

The app is deployed using **Render.com**, allowing public access to the prediction model through a simple web form built using HTML + CSS.

Frontend features:
- Clean upload form for CSV or manual input
- Displays prediction in ounces and kilograms

---

## 📁 Repository Structure

```
├── model_training.ipynb       # Jupyter notebook for model training
├── templates/
│   └── index.html             # Frontend UI (HTML)
├── app.py                     # Flask backend API
├── model.pkl                  # Saved ML model
├── requirements.txt           # Dependencies
├── README.md                  # This file
```

---

## ⚙️ How to Run Locally

```bash
# Step 1: Clone the repo
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

# Step 2: Create virtual environment
python -m venv venv
source venv/bin/activate    # On Windows: venv\Scripts\activate

# Step 3: Install dependencies
pip install -r requirements.txt

# Step 4: Run the app
python app.py
```

Navigate to `http://localhost:5000` in your browser to use the app.

---

## ⚠️ Key Insights & Limitations

While the model can provide **reasonably believable predictions**, there are a few important things to keep in mind:

- 📉 **R² Score ~ 0.2**: The model's R-squared value is relatively low, indicating that it doesn't capture all the variance in the data.
- 🧪 **Small Dataset (~1200 entries)**: The dataset is limited in size, which can impact the generalizability and accuracy of the predictions.
- 🤏 **Still Makes Sensible Predictions**: Despite these limitations, the model outputs values that make sense in real-world contexts.
- 🧠 **Educational Purpose**: This project is mainly intended to demonstrate the **end-to-end process** of ML model creation, deployment, and integration — rather than achieving high performance.
- 🔍 **Do Not Rely for Medical Use**: This is **not a medically certified model** and shouldn't be used in any real healthcare setting.

> 🧠 **Bottom Line**: It's a great proof of concept, but the accuracy can be significantly improved with more and better-quality data.

---
## 📌 Future Enhancements

- Switch to a more robust model (e.g., XGBoost or LightGBM)
- Include outlier removal and better preprocessing
- Add data visualization dashboard
- Deploy with Docker or on HuggingFace Spaces

---
## 👨‍💻 Author

Made with ❤️ by [Manmit Samal](https://github.com/manmit-s)

---
