# Deep-learning-challenge

Objective:

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. The purpose of this analysis is to use our knowledge of machine learning and neural networks and use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

The Data:  

From Alphabet Soup’s business team, we have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Results

        Step 1: Preprocess the Data
Using the knowledge of Pandas and scikit-learn’s StandardScaler(), we preprocess the dataset and identify the following in our dataset.

1. Read in the charity_data.csv to a Pandas DataFrame, and identify the following in the dataset:
   
.. What variable(s) are the target(s) for your model?
The target variable for our model is IS_SUCCESSFUL, a binary classifier that is 1 if the organization is successful and 0 if not.

.. What variable(s) are the features for your model?
The features for our model include:

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 34299 entries, 0 to 34298
Data columns (total 10 columns):
 #   Column                  Non-Null Count  Dtype 
---  ------                  --------------  ----- 
 0   APPLICATION_TYPE        34299 non-null  object
 1   AFFILIATION             34299 non-null  object
 2   CLASSIFICATION          34299 non-null  object
 3   USE_CASE                34299 non-null  object
 4   ORGANIZATION            34299 non-null  object
 5   STATUS                  34299 non-null  int64 
 6   INCOME_AMT              34299 non-null  object
 7   SPECIAL_CONSIDERATIONS  34299 non-null  object
 8   ASK_AMT                 34299 non-null  int64 
 9   IS_SUCCESSFUL           34299 non-null  int64 
dtypes: int64(3), object(7)
memory usage: 2.6+ MB

2. Droped the EIN and NAME columns.

3. Determined the number of unique values for each column.

4. For columns that have more than 10 unique values, we determined the number of data points for each unique value.

5. Used the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful.

6. Used pd.get_dummies() to encode categorical variables.

  Step 2: Compile, Train, and Evaluate the Model

Using the knowledge of TensorFlow, we designed a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. we thinked about that how many inputs there are before determining the number of neurons and layers in your model. Once completed that step,  compile, train, and evaluated binary classification model to calculate the model’s loss and accuracy.

Continue using the Jupyter Notebook in which we performed the preprocessing steps from Step 1.

Created a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.

Created the first hidden layer and choose an appropriate activation function.

If necessary, added a second hidden layer with an appropriate activation function.

Created an output layer with an appropriate activation function.

Checked the structure of the model.

Compile and train the model.

Created a callback that saves the model's weights every five epochs.

Evaluated the model using the test data to determine the loss and accuracy.

Save and export the results to an HDF5 file. Name the file AlphabetSoupCharity.h5.

    Step 3: Optimize the Model
    
Using the knowledge of TensorFlow, optimize model to achieve a target predictive accuracy higher than 75%.

Using any or all of the following methods to optimize your model:

Adjust the input data to ensure that no variables or outliers are causing confusion in the model, such as:
Dropping more or fewer columns.
Creating more bins for rare occurrences in columns.
Increasing or decreasing the number of values for each bin.
Add more neurons to a hidden layer.
Add more hidden layers.
Used different activation functions for the hidden layers.
Add or reduce the number of epochs to the training regimen.

Created a new Jupyter Notebook file and name it AlphabetSoupCharity_Optimzation.ipynb.

Import dependencies and read in the charity_data.csv to a Pandas DataFrame.

Preprocess the dataset like we did in Step 1, and adjust for any modifications that came out of optimizing the model.

Design a neural network model, and adjust for modifications that will optimize the model to achieve higher than 75% accuracy.

Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity_Optimization.h5.


Summary: 
Summarized the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.







