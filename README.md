# diabetes_ml

1. kaggle link: https://www.kaggle.com/code/zabihullah18/diabetes-prediction
2. 新数据：Dataset (14变量1k行): https://www.kaggle.com/datasets/aravindpcoder/diabetes-dataset/data 

## Outline

1. Data pre-processing，参考noteboook：https://www.kaggle.com/code/alexteboul/diabetes-health-indicators-dataset-notebook
  -  处理重复值：基于no_patient，no_patient相同的行中，（1）若其他变量都相同，则保留一个；（2）若其他变量存在不同，则全部删除。（assumption: 数据为同一时刻）
  -  （先画箱形图/小提琴图）按照标准差去掉outliers，进行标准化。
  -  去掉class=p的，因为我们要预测，要做二分类。
  -  gender，class变成0-1.
2. Feature selection: (e.g. combined with report of CDC)
   - Lasso, ridge regression
   - Correlation graph
5. Visualization: EDA
6. Classification: machine learning methods
7. Model validation: cross validation
