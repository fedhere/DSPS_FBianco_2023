- Download the Higgs boson data from Kaggle (programmatically within the notebook, see how in the Titanic notebook)

- Inspect, explore, clean the data as appropriate (missing values, however they encoded them, remove variables that should not be used etc)

- Split the provided training data into a training and a test set. For each model, you should calculate and discuss the training and test score results.

- Use a _Random Forest and a Gradient Boosted Tree **Classifier**_ model to predict the label of the particles.

- Produce a confusion matrix for each model and compare them

DSPS 661 students (EC for 461)
    
   - Use a _Random Forest and a Gradient Boosted Tree **Regressor**_ model to predict the weight of the particles.

   - Calculate the L1 and L2 metrics of each model and compare them.

Both 661 and 461 students choose either: 

  
   - For the _Random Forest Classifier_, select the 4 most important features (see how in the Titanic notebook) 
 
or  
   - For the _Random Forest Classifier_, explore the parameter space with the sklearn module sklearn.model_selection.RandomizedSearchCV for a model that uses only those features to predict the labels https://scikit-learn.org/stable/auto_examples/model_selection/plot_randomized_search.html#sphx-glr-auto-examples-model-selection-plot-randomized-search-py

  - Generate an ROC curve plot for the best model and discuss it https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_curve.html or https://scikit-learn.org/stable/auto_examples/model_selection/plot_roc_crossval.html#sphx-glr-auto-examples-model-selection-plot-roc-crossval-py
