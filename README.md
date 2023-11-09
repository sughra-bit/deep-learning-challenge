# deep-learning-challenge

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

Outcomes:

What variable(s) are the target(s) for your model?

The target for our model is IS_SUCCESSFUL, a binary classifier that is 1 if the organization is successful and 0 if not.

What variable(s) are the features for your model?

The features for our model include:

APPLICATION_TYPE: A categorical value for which we created a cutoff point to bin "rare" categorical variables together in a new value, Other and then proceeded to one-hot encode.
AFFILIATION: A categorical value that we one-hot encode.
CLASSIFICATION: A categorical value for which we created a cutoff point to bin "rare" categorical variables together in a new value, Other.
USE_CASE: A categorical value that we one-hot encode.
ORGANIZATION: A categorical value that we one-hot encode.
STATUS: A categorical value that we one-hot encode.
INCOME_AMT: The income amount is displayed in bins and is thus a categorical value that we one-hot encode.
SPECIAL_CONSIDERATIONS: A binary value with Y/N values. We used binary encoding to map Y/N to 1/0.
ASK_AMT: A float value.
All feature columns were split into training and testing values, and then scaled based on the training data using StandardScaler.
