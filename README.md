# Steel Temperature Prediction for Energy Optimization

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Machine learning model predicting molten steel temperatures in metallurgical plants to optimize electricity consumption and reduce production costs.**

**Author:** Ekaterina Bremel  
**Project Type:** Regression, Industrial ML  
**Status:** Completed

---

## 🎯 Project Overview

Built a regression model for "Temper Steel" metallurgical plant to predict steel temperatures during the processing stage, enabling more efficient control of the heating process and reducing energy costs. The model processes real-time industrial data from multiple sources to forecast final temperatures within 6°C accuracy.

### Business Impact
- **Goal:** Reduce electricity consumption during steel processing
- **Challenge:** Predict optimal steel temperature to minimize unnecessary heating cycles
- **Solution:** ML model that forecasts final temperature based on processing parameters
- **Result:** Successfully achieved MAE < 6°C, meeting production optimization requirements

---

## 📊 Dataset Description

The project uses data from a 100-ton metal ladle steel processing facility. Steel is heated with graphite electrodes, alloyed with various materials, and processed through multiple heating/measurement cycles until reaching target temperature and composition.

**Data Sources:**
- `data_temp.csv` - Temperature measurements throughout processing
- `data_arc.csv` - Active power data during electrode heating
- `data_bulk.csv` - Bulk material additions (alloy pieces)
- `data_bulk_time.csv` - Timing of bulk material additions
- `data_gas.csv` - Inert gas purging data
- `data_wire.csv` - Wire alloy additions
- `data_wire_time.csv` - Timing of wire additions

**Key Features:**
- Initial and final temperature measurements
- Chemical composition data (multiple alloying elements)
- Processing time metrics
- Active power consumption
- Material addition quantities and timing

---

## 🛠️ Technical Approach

### 1. Data Preprocessing
- Merged 7 separate datasets by batch key
- Handled missing values and outliers
- Removed batches with incomplete measurements
- Feature engineering: calculated time differences, aggregated material additions
- Created unified dataset with initial temp, processing parameters → final temp

### 2. Exploratory Data Analysis
- Distribution analysis of temperature ranges
- Correlation analysis between features and target variable
- Identified key drivers: initial temperature, processing time, material quantities
- Visualization of heating cycles and patterns

### 3. Feature Engineering
- Time-based features (processing duration)
- Aggregated material additions
- Chemical composition ratios
- Power consumption metrics

### 4. Model Selection & Training
Compared multiple regression algorithms:

| Model | MAE | Performance |
|-------|-----|-------------|
| **RandomForestRegressor** | **4.05** | ✅ Best |
| CatBoostRegressor | 5.46 | Good |
| LinearRegression | Higher | Baseline |

**Final Model:** RandomForestRegressor
- **Training Strategy:** 75/25 train-test split
- **Evaluation Metric:** Mean Absolute Error (MAE)
- **Cross-validation:** Used to prevent overfitting

### 5. Model Evaluation
- MAE on test set: **4.05°C**
- Well below target threshold of 6°C
- Consistent performance across temperature ranges
- Ready for production deployment

---

## 🚀 Key Results

✅ **MAE: 4.05°C** - Exceeded target accuracy (< 6°C)  
✅ **Production-ready** - Model can be integrated into steel processing workflow  
✅ **Energy optimization** - Enables precise temperature control, reducing unnecessary heating  
✅ **Cost reduction** - Fewer heating cycles = lower electricity consumption

---

## 💻 Technologies Used

**Languages & Libraries:**
- Python 3.8+
- Pandas - Data manipulation
- NumPy - Numerical computations
- Scikit-learn - Machine learning models
- CatBoost - Gradient boosting
- Matplotlib - Data visualization
- Seaborn - Statistical plotting

**Machine Learning:**
- Regression algorithms
- Ensemble methods (Random Forest)
- Feature engineering
- Cross-validation
- Hyperparameter tuning

---

## 📁 Project Structure

```
steel-temperature-prediction/
├── index.html              # Full analysis notebook (HTML export)
├── README.md              # This file
└── data/                  # (Data files not included - proprietary)
    ├── data_temp.csv
    ├── data_arc.csv
    ├── data_bulk.csv
    ├── data_bulk_time.csv
    ├── data_gas.csv
    ├── data_wire.csv
    └── data_wire_time.csv
```

---

## 🔍 View Full Analysis

**[👉 View Interactive Notebook (HTML)](index.html)**

The complete analysis includes:
- Detailed EDA with visualizations
- Feature engineering process
- Model comparison and selection
- Performance evaluation
- Code implementation

---

## 📈 Sample Visualizations

The project includes:
- Temperature distribution histograms
- Correlation heatmaps between features
- Predicted vs. Actual temperature scatter plots
- Feature importance analysis
- Model performance comparison charts

---

## 🎓 Skills Demonstrated

**Data Science:**
- Data cleaning and preprocessing
- Exploratory data analysis
- Feature engineering
- Regression modeling
- Model evaluation and validation

**Machine Learning:**
- Ensemble methods (Random Forest)
- Gradient boosting (CatBoost)
- Hyperparameter tuning
- Cross-validation techniques
- Performance optimization

**Business Understanding:**
- Translating business problem into ML task
- Defining success metrics aligned with business goals
- Industrial process optimization
- Cost-benefit analysis

**Tools & Technologies:**
- Python data science stack
- Scikit-learn ecosystem
- Statistical analysis
- Data visualization

---

## 🌟 Future Improvements

- **Real-time prediction:** Deploy model as API for live temperature forecasting
- **Additional features:** Incorporate external factors (ambient temperature, equipment age)
- **Deep learning:** Experiment with neural networks for complex pattern recognition
- **Monitoring:** Build dashboard for tracking model performance in production
- **A/B testing:** Compare energy savings with/without model predictions

---

## 📧 Contact

**Ekaterina Bremel**
- LinkedIn: [Ekaterina Bremel](https://www.linkedin.com/in/ekaterina-bremel-65b1b1238/)
- Email: bremelket@gmail.com
- GitHub: [@bremelket](https://github.com/bremelket)
---

## 📝 License

Copyright © 2026 Ekaterina Bremel. All rights reserved.

This project is available for viewing as part of my portfolio. Unauthorized copying, modification, distribution, or use of this code is prohibited.

---

**⭐ If you find this project interesting, please consider giving it a star!**
