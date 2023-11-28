- Download the Higgs boson data from Kaggle (programmatically within the notebook, see how in the Titanic notebook)

- Inspect, explore, clean the data as appriopriate (missing values, however they encoded them, remove variables tha should not be used etc)

- Split the provided training data into a training and a test set. For each model you should calculate and discuss the training and test score results.

- Use a _Random Forest and a Gradiend Boosted Tree **Classifier**_ model to predict the label of the particles.

- Produce a confusion matrix for each model and compare them

- Use a _Random Forest and a Gradiend Boosted Tree **Regressor**_ model to predict the weight of the particles.

- Calculate the L1 and L2 metrics of each model and compare them.

Either: 
- do 
  
   - For the _Random Forest Classifier_, select the 4 most important features (see how in the Titanic notebook) 
 
or  
- do
   - For the _Random Forest Classifier_, explore the parameter space with the sklearn module sklearn.model_selection.RandomizedSearchCV for a model that uses only those features to predict the labels https://scikit-learn.org/stable/auto_examples/model_selection/plot_randomized_search.html#sphx-glr-auto-examples-model-selection-plot-randomized-search-py

  - Generate an ROC curve plot for the best model and discuss it https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_curve.html or https://scikit-learn.org/stable/auto_examples/model_selection/plot_roc_crossval.html#sphx-glr-auto-examples-model-selection-plot-roc-crossval-py

- EC and 661

  - Download the script provided in the kaggle challenge to validate your model.

  - Generate an output file as required by this script for your best model

  - Report on the result

