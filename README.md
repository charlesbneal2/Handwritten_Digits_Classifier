# Handwritten Digits Classifier: Project Overview
- Compared KNN and neural network models to predict handwritten digits from UCI Machine Learning Repository
- Optimized parameters for each model to find best performance. Both models converged near 98% accuracy, with the KNN model performing slightly better. 

## Code and Resources Used
**Python Version:** 3.7

**Packages:** pandas, matplotlib, numpy, sklearn

**Dataset:** http://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits (included in Scikit-learn's library)

## Data Overview
Each image is represented as a row of pixel values and comes with a human-generated classification. We reconstructed some example images on 8x8 grids:

![image](https://user-images.githubusercontent.com/97380323/173472378-be0aa009-a6a3-4fb4-8e4e-f6a1129403cd.png)

## K Nearest Neighbors Model
I implemented a KNN classifier with 4-fold cross-validation and varied the number of nearest neighbors from 1 to 20 to find the best model.

![image](https://user-images.githubusercontent.com/97380323/173472491-59fbf5f1-5810-43c7-8a01-e4d57e8dcd0f.png)

A model using only one nearest neighbor demonstrated the best performance, with around 98% accuracy.

## Neural Network Model
I implemented a neural network classifier. I varied the number of hidden layers from 1 to 3, and varied the number of neurons per layer for each number of layers. I used 4-fold cross validation for the one and two layer models and 6-fold cross-validation for the three layer model to reduce overfitting.

![image](https://user-images.githubusercontent.com/97380323/173472675-c4916e9a-834b-4fb5-8f5e-67312e6033e1.png)

![image](https://user-images.githubusercontent.com/97380323/173472689-0b259c1d-1032-42bf-8910-30a3b76976f8.png)

![image](https://user-images.githubusercontent.com/97380323/173472706-96d94383-2731-4864-91cc-81dae69b4d0c.png)

With three layers, the model converges on just under 98% accuracy. For this problem, the KNN is a slightly better classifier and, because it is less computationally expensive, I would recommend it over the NN.

