# 🔥 Calorie Deficit Predictor  (MLR)

A public, static web application that estimates **daily calorie deficit or surplus** using a **Multiple Linear Regression (OLS)** model trained on the following dataset from Kaggle: https://www.kaggle.com/datasets/jockeroika/life-style-data.

This project is designed as an **educational and analytical demonstration** of applying statistical modeling to real-world health and fitness data, NOT as medical or nutritional advice.

---

## 🚀 Live Demo
Hosted as a static site (no backend, no tracking):

👉 **[Open the Predictor](https://abmarz.github.io/predical/)**  

---

## 🧠 What This Model Predicts

The output represents a **predicted calorie balance**:

- **Positive value (green)** → Estimated **calorie deficit**
- **Negative value (red)** → Estimated **calorie surplus**

The model does **not** predict calorie intake or burn independently, it predicts the *net balance* based on the provided variables.

---

## 📊 Model Overview

The predictor uses an **Ordinary Least Squares (OLS) Multiple Linear Regression** with the following structure:

Workout types are encoded as **indicator variables**:
- HIIT = 1 if selected, else 0  
- Strength = 1 if selected, else 0  
- Yoga = 1 if selected, else 0  
- Cardio / Other is the reference category

---

## 🧩 Input Variables Explained

| Variable | Description |
|--------|------------|
| **Session Duration** | Total training time for the day (in hours). Use 0 if no workout. |
| **Workout Type** | Primary workout type for the day (longest or most frequent). |
| **Weight** | Body weight at the time of the session (lbs). |
| **Age** | Age in years. |
| **Experience Level** | Self-reported fitness experience on a **1–5 scale**. |
| **Workout Frequency** | Average workouts per week (floats allowed). |
| **Physical Exercise** | **Categorical level (1–4)** representing general daily activity outside structured workouts. |
| **Proteins** | Daily protein intake (grams). |
| **Sugars** | Daily sugar intake (grams). |

> ⚠️ **Note on Physical Exercise**  
> This variable exists as a **1–4 categorical feature in the original dataset** with no formal definition.  
> The labels shown in the UI are inferred for usability and may not perfectly reflect the dataset’s intent.

---

## 🧑‍💻 Tech Stack

- **HTML / CSS / JavaScript**
- **No backend**
- **No user data stored**
- **Hosted via GitHub Pages**

The entire model runs client-side for transparency and simplicity.

---

## 📄 Report & Methodology

A full written report explaining:
- Data source
- Feature selection
- Model assumptions
- Limitations
- Interpretation guidelines

is available directly in the website under **“More about the model”**, or as a standalone PDF in the repository labelled `report.pdf`

---

## ⚠️ Disclaimer of Accuracy & Liability

This project is provided **“as is” and “as available.”**  
Predictions may be inaccurate, incomplete, or inappropriate for individual circumstances.

- This is **not medical, fitness, or nutritional advice**
- Use at your own risk
- Always consult qualified professionals for health-related decisions

By using this project, you accept full responsibility for how the output is interpreted or used.

---

## 👤 Author

**Abdullah Al Marzouq**  
🔗 [https://abmarz.com](https://abmarz.com)

Model design, analysis, and implementation by the author.

---

## 📌 License

This project is released for **educational and demonstration purposes only**.  
Reuse is permitted with attribution.
