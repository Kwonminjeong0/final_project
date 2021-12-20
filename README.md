# final_project

------------

### Model
> LinearSVC was used among linear SVM algorithms. 
> The support vector machine is a model that can solve classification problems well among machine learning models. 
> The SVM is a model in which a reference line for classification defines a decision boundary, and depending on the dimension, this boundary can be a line or plane. 
> The support vector of the support vector machine refers to data near the decision boundary that will determine the decision boundary decisively. 
> Among them, linear SVC is similar to SVC in which kernel is set to linear.
> But while defaulting scaling, SVC minimizes regular aging loss, and linear SVC minimizes the square aging loss.

### Hyper parameter
> LinearSVC's hyper parameters include penalty, loss, dual, tool, C, multi_class, fit_intercept, intercept_scaling, class_weight, verbose, random_state, and max_iter. 
> Penalty is used to determine whether the criterion to be used to give a penalty is l1 or l2, and tol is used to determine the tolerance value, and loss is used to specify the loss function. 
> Dual is a parameter that can control duality and tol is used to determine the tolerance value. 
> The intensity of the constraint can be set with C, the maximum number of repetitions can be specified with max_iter, three or more can be specified with multi_class, and the amount of learning can be adjusted with class_weight. 
> fit_intercept decides wheter to calculate the intercept for its model or not.

### code
------------
```python
from sklearn.svm import LinearSVC
```
 To use LinearSVC, I loaded additional acikit svm learn package.
 
```python
model = inearSVC(C=1, max_iter = 10000000)
```
I used LinearSVC so I created model with it.
If it executed with default value, it warns me that warnings.warn("Liblinear failed to converge, increase ".
So I increased max_iter.

```python
model.fit(X_train,y_train)
y_pred = model.predict(X_test)
```
And these are codes to fit the object to training dataset and predict the label of test data point.
