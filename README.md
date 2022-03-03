2022工研院第四梯次AI與資料科學人才訓練班，AIDEA平台上的課程競賽

## 原始檔案說明
1. train.csv: 長照機構的訓練資料集，所有參數都已經被模糊化；預測目標一共分三類，對應到檔案中的Y；其中Y = 2的類別非常少，屬於不平衡分類問題
2. test.csv: 測試資料集，欄位除了Y以外都與訓練資料集相同；共300筆資料

## model建立流程
1. 無缺值，全部欄位都屬於dummy variable
2. 使用Random forest model(RF model)進行變數挑選；建立30個RF model確認變數重要性的排序，篩選大於重要性 > 0.02的變數進行模型建立；另也使用Chi-square挑選12個最重要的變數
3. 使用xgboost model建立模型；調整參數；使用logloss做為metric 。
