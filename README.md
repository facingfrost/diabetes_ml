# diabetes_ml

1. kaggle link: https://www.kaggle.com/code/zabihullah18/diabetes-prediction
2. 新数据：Dataset (14变量1k行): https://www.kaggle.com/datasets/aravindpcoder/diabetes-dataset/data 

## Outline

1. Data pre-processing，参考noteboook：https://www.kaggle.com/code/alexteboul/diabetes-health-indicators-dataset-notebook
   - 处理重复值：基于no_patient，no_patient相同的行中，（1）若其他变量都相同，则保留一个；（2）若其他变量存在不同，则全部删除。（assumption: 数据为同一时刻）
   - （先画箱形图/小提琴图）按照标准差去掉outliers，进行标准化。
   - 去掉class=p的，因为我们要预测，要做二分类。
   - gender，class变成0-1.
   - diabetes_14.csv是原始数据，df_cleaned是process之后的数据
2. Feature selection: (e.g. combined with report of CDC)
   - Lasso, ridge regression
   - Correlation graph
   - Feature selection的结果：
   Lasso selection: ['HbA1c', 'BMI']

   Logistic selection: ['Gender', 'AGE', 'Urea', 'HbA1c', 'Chol', 'TG', 'HDL', 'LDL', 'VLDL', 'BMI']
       
   Ridge selection: ['Gender', 'AGE', 'Urea', 'Cr', 'HbA1c', 'Chol', 'TG', 'HDL', 'LDL', 'VLDL', 'BMI']
3. Visualization: EDA
   - 参考：https://www.kaggle.com/code/zabihullah18/diabetes-prediction#1-|-Introduction
4. Classification: machine learning methods
   - 参考：https://www.kaggle.com/code/zabihullah18/diabetes-prediction#1-|-Introduction
5. Model validation: cross validation
   - 参考：https://www.kaggle.com/code/zabihullah18/diabetes-prediction#1-|-Introduction
   - 同时加上cross validation
   - model selection：选个最好的
