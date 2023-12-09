## randomForest Package Intro

### Description

randomForest implements Breiman's random forest algorithm (based on Breiman and Cutler's original Fortran code) for classification and regression. It can also be used in unsupervised mode for assessing proximities among data points.

Original URL: <https://github.com/cran/randomForest/tree/master>

website URL: <https://jhu-statprogramming-fall-2023.github.io/biostat777-project3-part1-yijia0802/>

### Original Author

Fortran original by Leo Breiman and Adele Cutler, R port by Andy Liaw and Matthew Wiener.

#### Website Editor

Christiana Liu

### Functions

1.  **important**

    This is the extractor function for variable importance measures as produced by randomForest.

2.  **na.roughfix**

    This imputes Missing Values by median/mode.

3.  **outlier**

    This computes outlying measures based on a proximity matrix.

4.  **classCenter**

    Prototypes are \`representative' cases of a group of data points, given the similarity matrix among the points. They are very similar to medoids. The function is named \`classCenter' to avoid conflict with the function **`prototype`** in the **`methods`** package.

5.  **imports85**

    This is the \`Automobile' data from the UCI Machine Learning Repository.

6.  **getTree**

    This function extract the structure of a tree from a **`randomForest`** object.

7.  **MDSplot**

    This plots the scaling coordinates of the proximity matrix from randomForest.

8.  **margin**

    This computes or plots the margin of predictions from a randomForest classifier.

9.  **grow**

    This adds additional trees to an existing ensemble of trees.

10. **combine**

    This combines two more more ensembles of trees into one.

11. **rfcv**

    This function shows the cross-validated prediction performance of models with sequentially reduced number of predictors (ranked by variable importance) via a nested cross-validation procedure.

12. **plot.randomForest**

    This plots the error rates or MSE of a randomForest object.

    Example:

    ```         
    set.seed(71)
    iris.rf <- randomForest(Species ~ ., data=iris, importance=TRUE,
                            proximity=TRUE)
    plot(iris.rf)
    ```

13. **partialPlot**

    Partial dependence plot gives a graphical depiction of the marginal effect of a variable on the class probability (classification) or response (regression).

14. **treesize**

    This computes the size of trees (number of nodes) in and ensemble.

15. **randomForest**

    This implements Breiman's random forest algorithm (based on Breiman and Cutler's original Fortran code) for classification and regression. It can also be used in unsupervised mode for assessing proximities among data points.

    Example:

```         
set.seed(71)
iris.rf <- randomForest(Species ~ ., data=iris, importance=TRUE,
                        proximity=TRUE)
print(iris.rf)
```

16. **predict.randomForest**

    This is the prediction of test data using random forest.

17. **varUsed**

    This finds out which predictor variables are actually used in the random forest.

18. **rfImpute**

    This imputes missing values in predictor data using proximity from randomForest.

19. **tuneRF**

    Starting with the default value of mtry, search for the optimal value (with respect to Out-of-Bag error estimate) of mtry for randomForest.

20. **varImpPlot**

    Dotchart of variable importance as measured by a Random Forest

21. **rfNews**

    Show the NEWS file of the randomForest package.
