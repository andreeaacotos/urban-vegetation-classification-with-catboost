# Urban Vegetation Classification with CatBoost 🌳🌍


This repository presents the methodology for classifying vegetation in urban areas using **CatBoost**, a powerful gradient boosting algorithm 📈. 

The project is part of Omdena's Local Chapter challenges: [**Standardized Comparison of Urban Green Space Mapping Through Remote Sensing for Frankfurt, Germany**](https://www.omdena.com/chapter-challenges/standardized-comparision-of-urban-green-space-mapping-through-remote-sensing), aiming to address the challenge of detecting and mapping small urban green spaces using machine learning and deep learning techniques. 🌳🌍📸 

This initiative focuses on leveraging advanced algorithms to enhance the accuracy and efficiency of urban vegetation classification. By combining high-resolution satellite imagery with innovative computational methods, the project seeks to create robust solutions for monitoring urban greenery, ultimately contributing to sustainable urban planning and environmental preservation. 🌱

## Overview 📊

The notebook `catboost_Omdena.ipynb` includes the following steps:

1. **Environment Setup** ⚙️
   - Install necessary Python packages including `numpy`, `scikit-learn`, `CatBoost`, `rasterio`.
   - Setup DagsHub client for data downloading 🌐.

2. **Data Preparation** 📂
   - Download and load remote sensing data using DagsHub 📥.
   - Load images and masks from the downloaded data 🖼️.
   - Preprocess the images and masks for the model.

3. **Exploratory Data Analysis** 🔍
   - Visualize sample images and masks to understand the dataset structure 📉.

4. **Preprocessing and Training the CatBoost Model** 
   - Extract relevant bands from the masks to create a binary vegetation mask 🌿.
   - Flatten the images and prepare the target labels for binary classification 🔢.
   - Handle class imbalance by calculating class weights ⚖️.
   - Split the data into training, validation, and test sets 🔄.
   - Initialize and train the CatBoost model with class weights and validation set 🧠.

5. **Model Evaluation** 📏
   - Evaluate the trained model on the test set using various metrics including precision, recall, F1-score, and ROC-AUC score 🎯.
   - Visualize feature importance and ROC curve 📈.
   - Plot training and validation metrics over epochs 📊.
   
   #### More Details: 
   The model is trained on a large dataset with optimized hyperparameters to enhance predictive accuracy. Performance is evaluated using standard classification metrics, including **precision**, **recall**, **F1-score**, and **ROC-AUC score**, ensuring a robust assessment of the model's effectiveness 🎯.

   ### Key Results 📊
   - **Overall Accuracy:** 91% ✅  
   - **Precision for Vegetation:** 98% 🌿  
   - **Recall for Vegetation:** 91% 🔍  
   - **ROC-AUC Score:** 0.97 📈  

   The confusion matrix reveals that most vegetation areas are correctly classified, though some non-vegetation pixels are misclassified as vegetation. 
   These results highlight CatBoost's strong predictive capability and reliability for urban vegetation classification 🌍.

6. **Model Inference** 🔮
   - Upload test images and evaluate the model's performance on new data 🆕.

### Notebook Details 📓

### Environment Setup ⚙️

```python
# Install necessary packages
!pip install numpy==1.25.2 scikit-learn catboost pyrsgis rasterio focal-loss segmentation_models dagshub
```

---

## Conclusion 🎯
CatBoost proves to be a highly effective and computationally efficient solution for urban vegetation mapping, achieving good performance metrics. 
This approach demonstrates its potential for real-world applications in remote sensing and urban green space monitoring 🌱🛰️.
