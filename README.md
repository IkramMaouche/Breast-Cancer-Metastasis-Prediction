# eXplainable Breast Cancer Metastasis Prediction 

This project implements a machine learning model that classifies patients using a cost-sensitive CatBoost classifier. The purpose of this project is to provide an automated method for identifying patients with metastasis risk. The quantification of predictive factors on metastasis is measured using LIME technique.

##Prerequisites

pip==23.0.1
python==3.10.11
matplotlib==3.7.1
pandas==1.5.3
joblib== 1.2.0


Sciait-learn==1.1.2
scikit-plot== 0.3.7
missingpy==0.2.0

deap==1.3.3
lime== 0.2.0.1

xgboost==0.90
lightgbm==2.3.1
catboost==1.1


##Code Structure

The code for this project is organized into several sections:
1. Data loading: This section contains the code that loads the dataset into pandas data frame from excel file, cleaning the data, and converting categorical variables into numerical variables using label encoding.
2. Data imputation: handling missing value using missForest.
3. Data splitting and under-sampling: This sections contains the code for splitting the data into 80% training and 20% test ing instances. Then, under-sampling the majority class using Edited Nearest Neighbor (ENN).
4. Feature selection: contains functions the implementation of genetic algorithm for feature selection.
5. LR, DT, KNN classification: This section contains the implementation of the three classifiers LR, DT, and KNN. The models are fitted on training data, evaluated with test data, and saved in « .pkl » format. 
6. Cost insensitive  classification: This section contains the implementation of the three boosting classifiers XGBoost, LightGBM, and CatBoost. The models are fitted on training data, evaluated with test data, and saved in « .pkl » format. 
7. Cost sensitive  classification: This section contains the implementation of the three cost-sensitive boosting classifiers CS-XGBoost, CS-LightGBM, and CS-CatBoost. The models are fitted on training data, evaluated with test data, and saved in « .pkl » format.
8. Local explanation using LIME: This section contains the employment of LIME to provide patient-level explanations on breast cancer metastasis.

- The code was implemented and executed on google colab.

- If you wish to run the code from scratch you can execute all the code sections sequentially.

- Each section could be executed independently from previous section, you can just upload the required data file which can be found in the "data" file.

- If you do not wish to fit the models, the fitted models on the train data are saved in "models" file, you may upload them and run the evaluation code to generate the confusion matrices.

- To run lime explanation code, you may load the saved CS-CatBoost model which is saved in "models" file and run the code.



##Results
The data are stored in a separate file "data".
The fitted models are saved in "models" file in pol format.
The resulted confusion matrices from evaluating the classifiers are presented in folder "figures". 

