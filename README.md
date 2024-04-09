# Module21_Neural_Networks
## A report on the performance of the deep learning model you created for Alphabet Soup.

### Overview of the analysis
The purpose of this analysis is to create a model that helps it select the applicants for funding with the best chance of success in their ventures. That way, Alphabet Soup can focus funding on ventures that will prove successful.

### Data Preprocessing
#### What variable(s) are the target(s) for your model?
The target variable, or y value, for the model is: is "IS_SUCCESSFUL" or the boolean yes/no that a project was successful or not
The model is to predict (y) if the campaign was successful or not.

#### What variable(s) are the features for your model?
The features, or x values, are, "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT" 
Based on these x values, the model will try to predict how each x bears change on y

#### What variable(s) should be removed from the input data because they are neither targets nor features?
Perhaps "APPLICATION_TYPE" and "CLASSIFICATION" should be removed as the other columns might have enough weight to cause change in y. This is categorical data, but also doesn't tell much about the application. It also has several different options to be categorized under, but not much to say.
Meanwhile, another column such as "AFFILIATION" might be a useful feature. This is because independent (or, unsupported) ventures might struggle more to be successful than a company sponsored venture.

### Compiling, Training, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model?
Considering there were several categorical fields (that then were converted to binary), the model ended up with two activation functions and two layers with 80 and 30 neurons each. 

#### Were you able to achieve the target model performance?
No. While the model did achieve 0.7253644466400146 or 72% accuracy, that is below the 90% or higher accuracy preferred for business purposes. 
The model had 43 different inputs as well, which might have limited efficiency since so many features, some unnecessary, had to be considered.

#### What steps did you take in your attempts to increase model performance?
In the future, implementing a function to test several more hyperparameter combinations would be optimal to increase accuracy. 

#### Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
Overall, the results showed the model predicted with 72% accuracy. 
A different model would solve this problem better because a different model would have less inputs (and thus more focused data) and higher accuracy. 
My reccomendation is to create a function that tests different possible combinations of models, as well as reduce the amount of inputs fed into the model. 
For the newer model, the analyst (and organization) should consider closely if each input feature really does have enough impact on target values to be included. For example, removing application type from the inputs.
As well as continuing to refine the model. As new data comes in, the analyst should keep refining whether features are useful, and if previously dropped features have more impact than previously thought. 

To put it shortly: less inputs, more layers, more variety on application type 
