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


TO GET THE DATA

Please register for an account at kaggle.com, all the work we will do together in class as well as your next homework will require it. To register do the following:

go to kaggle.com

click on “Register” in the upper right corner select either Register with Google, or Register with your email (it’s up to you)
follow the instructions provided by kaggle to create an account (enter your email address, create a password, and choose a username), all of which are up to you, this will be your account after all
Make sure that at the end, you have an account that you can log in with, and be logged in and ready next class


- Go to https://www.kaggle.com/ and sign in

- Click on the icon of your avatar on the top right
![image](https://github.com/fedhere/DSPS_FBianco/assets/1696902/1dffcf40-a2e9-48fb-a499-c14a27dcfe6c)

- select "Settings" from the drop menu
![image](https://github.com/fedhere/DSPS_FBianco/assets/1696902/201c1138-b25c-4999-9b97-13db959a9ec1)

- scroll down to API and click create New API Token. This will download a json file on your computer

![image](https://github.com/fedhere/DSPS_FBianco/assets/1696902/6fc04ffa-9dbc-4699-9173-7757512f62d1)
![image](https://github.com/fedhere/DSPS_FBianco/assets/1696902/977dfab6-4adb-4471-bb3a-cbf9f1c5406c)


- open google drive at https://drive.google.com/drive/u/0/my-drive in your browser
- upload (e.g. dragna and drop) the kaggle.json file from your laptop to the drive

  ![image](https://github.com/fedhere/DSPS_FBianco/assets/1696902/57841c2d-1aa0-4c5b-a65e-9803cea3a181)

- the rest of the information are to be done on your colab notebook: follow accordingly (see what was done in the Titanic notebook in ClassDemos)

```
# this mounts your google drive
from google.colab import drive
drive.mount("/content/gdrive")

# this gets you to your drive folder
cd gdrive/My\ Drive/

# this makes sure the file is there: this cell should return "kaggle.json"
ls kaggle.json

# this limits who can view and make changes who can access this file.
!chmod 600 kaggle.json

# this reads in the file and stores it into the system variables of your colab sessions which allows you to connect programmatically to the kaggle platform
envs = json.load(open("kaggle.json", "r"))
os.environ["KAGGLE_USERNAME"] = envs['username']
os.environ["KAGGLE_KEY"] = "e60b57c215e877e01a22375a3058eec1"#envs['key']
