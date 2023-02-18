# sampling-ucs654
This repository contains solution to sampling assignment for UCS654.

### List of tasks:
- [x] Download the [dataset](https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv) 
- [x] Convert it into balanced dataset
- [x] Create 5 samples
- [x] Apply 5 different sampling techniques on five different ML models

### Discussion:
The dataset used is highly imbalanced. The number of samples in the minority class is only 1.167% of the total number of samples. I used the SMOTE algorithm to oversample the minority class.

For sampling, I have used the following different techniques:

1. Random Sampling
2. Stratified Sampling
3. Cluster Sampling
4. Systematic Sampling

All five samples were then trained on the following ML models with K-Fold Cross Validation:

1. Logistic Regression (LR)
2. Decision Tree Classifier (CART)
3. K-Nearest Neighbours (KNN)
4. Random Forest Classifer (RF)
5. Bagging Classifier (BAG)

### Performace Evaluation:
The cross validation results for the different samples with different models are mentioned below.
|      | Random | Stratified | Cluster | Systematic |
|------|--------|------------|---------|------------|
| LR   | 0.837  | 0.901      | 0.926   | 0.911      |
| CART | 0.902  | 0.969      | 0.983   | 0.947      |
| KNN  | 0.781  | 0.872      | 0.964   | 0.822      |
| BAG  | 0.913  | 0.971      | 0.988   | 0.942      |
| RF   | 0.967  | 0.992      | 0.997   | 0.963      |

The accuracy of these models on test set is as follows:
|      | Random | Stratified | Cluster | Systematic |
|------|-------:|------------|---------|------------|
| LR   |  0.946 |    0.929   |  0.941  |    0.926   |
| CART |  0.913 |    0.945   |  0.987  |    0.905   |
| KNN  |  0.897 |    0.890   |  0.980  |    0.811   |
| BAG  |  0.946 |    0.950   |  0.993  |    0.921   |
| RF   |  0.989 |    0.982   |  0.993  |    0.953   |

Clearly, Random Forest Classifier consistently yields the highest accuracy across all sampling techniques.
