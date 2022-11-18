# Tissue_classification
Building an algorithm that classifies with high accuracy a breast tissue mass as either malignant or benign, whilst avoiding misclassification of a malignant tumor as benign. 

The data used in this project contained summarized information on the sample cells from Fine Needle Aspiration (FNA) of 569 breast tissue masses. The characteristics of the tissue mass included their respective radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, and fractal dimension. For each of these 10 characteristics, the mean, standard error of the mean, and maximum for each these values were included in the dataset and each breast tissue mass was labeled as either malignant or benign. 

The goal of the project is to demostrate how machine learning could be used in the evaluation of tumors in breast tissue masses. 

To start, I conducted exploratory data analysis (EDA) to see how the data behaved. First, I conducted a univariate relationship test between all of the predictor variables and the diagnosis. It was found that higher values in the explanatory variables are usually tied to malignant tissue masses compared to those classified as benign and that malignant tissues have a higher range of values for each of the variables vs benign tissues.

Additionally, I conducted a scatterplot test to see the relationship between the mean and standard error of the mean for each of the predictor variables. This showed that for most benign tissues there was a really tight positive relationship between mean and standard error whereas malignant tissues had a much more variance in the relationship but a distinctly positive one as well.


To test out some machine learning techniques and to see which yields the best results, I chose to use decision trees, random forests, and K-nearest neighbors. These are all supervised machine learning algorthims, in which the machine is given a training set, which is labeled data with the desired output. After training the model, it is expected that the algorithm will have an understanding of the data and will make correct predictions. 

Results of the models:

Decision Tree - An overall accuracy of 94.6% and a true positive rate of 98.5%, meaning that the algorithm will correctly detect malignant tissue mass 98.5% of the time. It also has a misclassification rate of 5.4%

Random Forest - An overall accuracy of 98.21%, a true positive rate of 98.59%, and a misclassification rate of 1.78%

K-nearest neighbor - When using K = 25, an overall accuracy of 93.8% was achieved, but with a true positive rate of 100%. This model has a misclassification rate of 6.3%

Although it would depend on which metrics the person building the model would deem most important, while the K-nearest neighbor has the highest true positive rate, I felt like the Random Forest was the best algorithm for predicting breast tissue mass as cancerous. The K-nearest neighbor had the lowest accuracy and the highest misclassification rate, while the random forest had both the highest accuracy and lowest misclassification rate. 
