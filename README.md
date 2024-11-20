# 💧 Water Quality Analysis

## 🌟 Introduction
Water is essential for all living beings, and access to clean drinking water is a fundamental human right. 🌍💦 However, water quality can be affected by many factors, making it crucial to analyze and determine its potability.

This project uses a Kaggle dataset that includes various key factors affecting water quality. The goal is to analyze these factors to determine whether the water is potable (safe to drink).

## 📊 Analysis Goals

To conclude if the water is potable or not, we will analyze:

- 🔍 Distribution of safe and unsafe water
- 🌡️ pH level of water
- 🧴 Hardness level
- 🌊 Dissolved solids
- 🧪 Chloramines concentration
- 🧂 Sulphate concentration
- ⚡ Conductivity of water
- 🌱 Organic carbon amount
- 🧫 Trihalomethanes concentration
- 🌫️ Turbidity of water

## 🚀 Steps in Analysis

### 📌 Data Preprocessing
1. `Handle Missing Values`: Dropping rows with null values.
2. `Target Variable`: Focused on the Potability column to classify water as safe or unsafe.

### 📈 Data Visualization
🔹 Distribution of Potable and Non-Potable Water
plt.figure(figsize=(15, 10))
sns.countplot(data.Potability)
plt.title("Distribution of Unsafe and Safe Water")
plt.show()

🔹 Analyzing Key Factors One by One:
- `pH Level`: Ideal range is 6.5–8.5.
- `Hardness`: Drinking water should have hardness between 120–200 mg.
- `Solids`: Indicates total dissolved solids in water.
- `Chloramines`: Used as a disinfectant in public water systems.
- `Sulphate`: Safe level is <500 mg.
- `Conductivity`: Should be less than 500 μS/cm.
- `Organic Carbon`: Safe drinking water has <25 mg.
- `Trihalomethanes (THMs)`: Safe level is <80 mg.
- `Turbidity`: Should be less than 5 NTU.

### 🛠️ Sample Code for Visualization

import plotly.express as px

figure = px.histogram(data, x="ph", color="Potability", title="Factors Affecting Water Quality: pH")
figure.show()

## 🔄 Correlation Analysis

I analyzed the correlation between pH and other factors to determine their relationship and impact on potability.

correlation = data.corr()
correlation["ph"].sort_values(ascending=False)

## 📉 Correlation Insights
### Pie Chart Representation

![image](https://github.com/user-attachments/assets/3f82e44d-de60-460d-9984-c0523f5db2a4)

This pie chart visualizes the correlation of pH with other water quality factors like hardness, organic carbon, and turbidity.

## 🏁 Conclusion
By analyzing the dataset, we assessed:

✅ pH level

✅ Hardness

✅ Organic carbon

✅ Conductivity

✅ Sulphate

✅ Trihalomethanes

✅ Chloramines

✅ Turbidity

This comprehensive analysis determines whether water samples are safe to drink, helping ensure access to potable water. 🌍💧

## 🛠️ Built With
- Python 🐍
- Pandas 🐼
- Matplotlib 📊
- Seaborn 🎨
- Plotly 🔎

## 🤝 Contributing
Feel free to fork this repository, raise issues, or submit pull requests. Let's make clean water analysis accessible to everyone! 🌟

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

## 🌟 Acknowledgments
Kaggle for the dataset.
The open-source community for incredible tools and libraries! 💻✨
