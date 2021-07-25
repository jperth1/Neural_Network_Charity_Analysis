# Neural_Network_Charity_Analysis

This analysis uses a deep learning neural network models to evaluate a binary classification on non-profit financial data. The data set contains information on whether non-profit organizations properly and successfully use the donations they received and includes data from the organization’s application. Using pandas, data is preprocessed using binning and encoded. Data is split data into features and target arrays, then fit and scaled. The model is compiled, trained, and evaluated using the preprocessed data. The initial dataset and model is designed to not reach 75% accuracy. Following the initial model and second model is created to reach an accuracy of 75% or higher. 

## Results:

### Data Preprocessing
-	The column “IS_SUCCESSFUL”  is the target for the model
-	Before encoding the object datatypes columns, the features used were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT 
-	For the columns that were object datatypes, the function OneHotEncoder() was used
-	The columns that were neither targets nor features were dropped. These were the EIN, NAME, and the original columns that were encoded.

### Compiling, Training, and Evaluating the Model
-	Two hidden layers are used for the neural network, the first using 80 neurons and the second using 30. ReLU is used as the activation function for the hidden layers and Sigmoid is used for the output layer. 
- The target accuracy was 75%, and our initial neural network was only able to achieve 72.4% accuracy.
- In efforts to reach 75% accuracy, additional columns were removed and further bucketing was performed. The neurons for the first hidden layer was changed to 102, the second changed to 74 neurons, and a third hidden layer was added that used 30 neurons. The number of epochs was changed to 90. These changes resulted in an accuracy of 75.5%

The images shown below illustrate the difference in accuracy percentages for the initial model and the second model

![accuracy_model_1](/Resources/accuracy_model_1.png)

![accuracy_model_2](/Resources/accuracy_model_2.png)

## Summary 
The results of the deep learning neural network model how that this is not the best model for this problem. After exploring various changes to improve the model the accuracy slightly improved. However, there are different tools that can be used to solve a binary classification problem, such as logistic regression, support vector machines, decision trees, and k-nearest neighbors. It is recommended that these models be used and evaluated for this dataset.
