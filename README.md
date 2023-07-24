# Task3_WideBot
## description of the whole training process in brief points
### Load Data :
To begin, we will load the data. As the data is distributed across various files, with each file containing information pertaining to a particular topic, we will need to iterate through the topics and consolidate the results by concatenating them.

We have nearly 1000 narratives for each subject, indicating that our dataset is evenly balanced.

### Data cleaning :

The data we are working with comprises Arabic text. To clean our data, we will follow a two-step process:

**Step 1** :  Eliminating stop words 

Certain words, such as "الذي" and "هو," occur frequently in all Arabic texts and do not provide any relevant information that our model can use to make predictions. By removing them, we can reduce noise and enable our model to concentrate solely on pertinent words. We will accomplish this by employing a list and iterating over all the articles to remove any words that appear in the list.

**Step 2** :  Punctuation removal 

To attain the same objective, we will also remove punctuation from the text data. I have utilized a regular expression (Regex) expression to achieve this.

### Data Split:

The data was divided into training and testing data, where 80% of the data was allocated for training and 20% for testing. The remaining 20% represents the test data consisting of the last 200 rows of data for each class.

### Build a machine learning based classifier 
We will try the following **SGDClassifier** , so we start to vectorize the input data using a CountVectorizer
and then create an instance of the SGDClassifier with a maximum of 1000 iterations and a tolerance of 1e-3    
after that we fitted the classifier to the vectorized training data and target variables

### Model Evaluation
It is the process that uses some metrics which help us to analyze the performance of the model. As we all know that model development is a multi-step process and a check should be kept on how well the model generalizes future predictions.

We show its performance on the test-set. Show precision, recall, f-score, accuracy for each class and for 
the whole test data.

