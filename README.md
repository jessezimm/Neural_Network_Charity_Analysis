# Neural Network Charity Analysis

# Overview 
 Using data from over 34,000 organizations that have received funding from Alphabet Soup over the years, this analysis is aiming to create a neural networl (binary classifier) that will predict whether applicants will be successful if funded by Alphabet Soup.

# Results
Model 1 Results

![image](https://user-images.githubusercontent.com/88340176/147962593-ac1519cf-e4bd-4677-be3b-748a1af0a618.png)

Model 2 Results

![image](https://user-images.githubusercontent.com/88340176/147962633-6bd5c86c-2cc4-47ba-970a-70640dc51e4a.png)

## Data Preprocessing
What variable(s) are considered the target(s) for your model?
* The target variable is "IS_SUCCESSFUL", which indicates whether or not the charity was successful after being funded by Alphabet Soup.

What variable(s) are considered to be the features for your model?
* The features are listed in the image below.

![image](https://user-images.githubusercontent.com/88340176/147959620-5f0618c8-cc71-4c30-a94c-05fa53fb42c7.png)

What variable(s) are neither targets nor features, and should be removed from the input data?
* "EIN" and "NAME" should be removed from the input data.

## Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
* For my initial neural network model, I selected two hidden layers with 9 neurons (for the nine features) the first layer and five neurons in the second layer. The activation functions I selected for mboth layers was the "ReLU" function because it is commonly-used and suitable for positive data, which fits the charity data provided.

* For my second attempt at building a neural network model and optimizing it, I selected three hidden layers with 9 neurons in the first layer, 7 in the second, and 6 in the third. The first two layers, I used the "ReLU" activation function and for the third layer, I used the "Sigmoid" activation function. I added the "Sigmoid" function in the third layer because it is ideal for binary classification, which is the goal of this model, and the data is positive and mainly categorical.

Were you able to achieve the target model performance?
* For my second attempt, my loss metric increased from 0.70 to 0.72, but my accuracy decreased from 0.58 to 0.53. The model did not achieve the target model performance of 75% accuracy.

What steps did you take to try and increase model performance?
* By adding an additional hidden layer, increasing the number of neurons for the second and third layer, and making the third layer's activation function a "Sigmoid", I was hoping to increase the accuracy of the model. I learned that adding more neurons and layers and altering the activation function for a layer does not necessarily improve the model. Sometimes less is more.

# Summary
Overall, a loss metric of 0.70 means the model poorly characterizes the data. Given that an accuracy cutoff for most neural networks in the healthcare industry is at least 95-99% accuracy, an accuracy of 58% is poor. To create a better model, I recommend adding more epoches (training iterations), which would increase the amount of information sent to each neoron, and likely create more effetive weight coefficients. Additionally, I would give any additional hidden layers the "ReLU" activation function because it will assess the input data differently without the risk of censoring or ignoring lower complexity inputs.
