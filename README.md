#  Breast Cancer Classification — Machine Learning Project

This project implements a complete classical Machine Learning pipeline for **breast cancer classification** using the **Breast Cancer Wisconsin (Diagnostic) Dataset**.  
It includes exploratory data analysis, dimensionality reduction, clustering, and supervised classification using a **Random Forest** classifier.

The goal is to distinguish **malignant** from **benign** tumors with high accuracy using interpretable ML techniques.

---

##  Dataset Overview
- **569 samples**
- **30 numerical features** extracted from digitized images of breast cell nuclei  
- **Binary target:**  
  - `0` = malignant  
  - `1` = benign  
- No missing values  
- Standard benchmark dataset in biomedical ML

---

##  Preprocessing
- Standardization with **StandardScaler**
- 80/20 train-test split (stratified)
- No missing values, no categorical encoding required

---

##  Exploratory Data Analysis (EDA)
The EDA explores:
- Class distribution
- Feature histograms
- Correlation heatmap
- Boxplots for key predictors

Clearly visible patterns show malignant tumors with:
- higher radius, perimeter, and area  
- more irregular and concave cell shapes

---

##  Dimensionality Reduction

### **PCA (Principal Component Analysis)**
- Projects data to 2D while maximizing variance  
- Shows partial separation between the two classes

### **LDA (Linear Discriminant Analysis)**
- Uses class labels to find the axis of maximum separability  
- Produces *near-perfect* linear separation

---

##  Clustering (Unsupervised)

### **K-Means (k = 2)**
- Applied after PCA  
- Clusters align closely with real tumor labels  
- Shows natural separability of the data

---

##  Random Forest Classifier (Final Model)

### **Results**
- **Accuracy:** 95.9%  
- **Precision:** 95.4%  
- **Recall:** 98.1%  
- **F1-Score:** 96.8%  

### **Confusion Matrix**
Very few false positives or false negatives — excellent diagnostic performance.

---

##  Feature Importance
Top predictive features:
- worst concave points  
- worst radius  
- worst perimeter  
These metrics capture irregularity and size of tumor cells.

---

##  Project Structure

