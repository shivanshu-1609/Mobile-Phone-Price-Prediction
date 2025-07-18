
# 📱 Mobile Price Range Prediction

This project predicts the **price range** of a mobile phone (Low, Medium, High, Very High) using various features like RAM, battery power, screen size, and more. It applies **machine learning models** such as **Logistic Regression** and **Random Forest** to classify the mobile price range accurately.

---

## 🧠 Problem Statement

> Predict the price category (0 to 3) of a mobile device based on specifications like:
- Battery power
- RAM
- Screen resolution
- Storage
- Camera specs
- Connectivity (3G/4G/WiFi, etc.)

---

## 📁 Dataset

The dataset (`dataset.csv`) includes **2000 samples** and **21 features**.  
Each mobile is labeled with a `price_range`:
- `0`: Low Cost
- `1`: Medium Cost
- `2`: High Cost
- `3`: Very High Cost

No missing values were found in the dataset.

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Joblib (for model saving)

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Correlation Matrix

A heatmap was used to analyze correlations among features.  
Helpful to identify multicollinearity and important predictors (e.g., RAM, battery power).

### 🔹 Feature Distributions by Price

Boxplots were created for:
- **RAM vs Price Range**: Strong positive relationship with price.
- **Battery Power vs Price Range**: Higher battery generally means higher price.

---

## ⚙️ Data Preprocessing

- **Features and Target Split**:  
  `X = df.drop('price_range', axis=1)`  
  `y = df['price_range']`

- **Feature Scaling**:  
  StandardScaler was used to normalize feature values.

- **Train-Test Split**:  
  80% Training and 20% Testing  
  `random_state=42`

---

## 🤖 Model Building

Two models were trained and evaluated:

### 🔹 Logistic Regression
- Accuracy: **97.75%**
- Excellent performance on all price classes.

### 🔹 Random Forest Classifier
- Accuracy: **89.25%**
- Slightly lower performance, especially in class `2`.

---

## 🧪 Model Evaluation

### ✅ Classification Reports (Precision / Recall / F1):

**Logistic Regression**:
| Class | Precision | Recall | F1-score |
|-------|-----------|--------|----------|
| 0     | 1.00      | 0.97   | 0.99     |
| 1     | 0.95      | 1.00   | 0.97     |
| 2     | 0.99      | 0.95   | 0.97     |
| 3     | 0.97      | 0.99   | 0.98     |

**Random Forest**:
| Class | Precision | Recall | F1-score |
|-------|-----------|--------|----------|
| 0     | 0.95      | 0.96   | 0.96     |
| 1     | 0.89      | 0.87   | 0.88     |
| 2     | 0.78      | 0.87   | 0.82     |
| 3     | 0.94      | 0.87   | 0.90     |

### 🔹 Confusion Matrices

Both models' confusion matrices were visualized using heatmaps to analyze misclassifications.

---

## 💾 Model Saving

The best-performing model (**Logistic Regression**) was saved using Joblib:

```python
joblib.dump(lr, 'logistic_model.pkl')
```

This allows future predictions without retraining.

---

## 📌 Project Structure

```
Mobile-Price-Prediction/
│
├── 📁 Data/                     # Contains datasets (train/test)
│   └── dataset.csv   # example data file
│
├── 📁 Model/                    # Contains saved models or model-related files
│   └── mobile_price_model.pkl         
│
├── 📁 Notebooks/               
│   └── mobile_price_prediction.ipynb
│
├── 📄Predict Mobile Phone Pricing.pdf
├── 📄 README.md                
├── 📄 requirements.txt         
├── 📄 .gitignore               # To ignore checkpoints, system files etc.

```

---

## 📦 Installation & Running

1. **Clone the repository**  
   ```
   git clone https://github.com/shivanshu-1609/Mobile-Phone-Price-Prediction.git
   cd Mobile-Phone-Price-Prediction
   ```

2. **Install dependencies**  
   ```
   pip install -r requirements.txt
   ```

3. **Run the notebook or Python script**

---

## ✅ Requirements

- Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- joblib
- IPython (for `display_html`)

You can install them via:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib ipython
```

---

## 📈 Future Work

- Improve accuracy using advanced models like XGBoost or SVM.
- Deploy the model with a Flask or Streamlit web app.
- Add feature importance visualization.

---

## 🙋‍♂️ Author

👨‍💻 **Shivanshu Shukla**  
BTech | AI & ML Enthusiast  
GitHub: [@shivanshu-1609](https://github.com/shivanshu-1609)

---

## 🌐 Connect

If you liked the project, leave a ⭐ on the repo!  
Feel free to connect with me on [LinkedIn](https://linkedin.com/in/shivanshu-shukla16/) for feedback, collaborations, or queries.

---
