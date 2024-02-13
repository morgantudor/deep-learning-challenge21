Challenge 21: Deep Learning

## Overview of the Analysis
In this activity, we were tasked with the challenge to create a tool for a non-profit organization, Alphabet Soup, that would assist them in screening investment applicants. This tool, if successful, would determine if applicants would be successful if their ventures were funded by the company. Data provided consisted of more than 34,000 organizations that received funding from the company in the past and various points of metadata about each organization. Utilizing this resource, model production began. 

## Results
# Data Preprocessing
* What variable(s) are the target(s) for your model?
  The target variable for this model will be the "IS_SUCCESSFUL" category because we want to train our model to identify if these campains will be successful.

* What variable(s) are the feature(s) for your model?
  The feature variables are all other columns/categories (except for EIN and NAME) because these factors are what are going to help our model determine whether or not a campaign will be successful.

* What variable(s) should be removed from the input data because they are neither targets nor features?
  In our model, we removed EIN & NAME categories because they were neither targets nor features as they were to niche of categories to provide insight into future success.

# Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
![nn1](https://github.com/morgantudor/deep-learning-challenge21/assets/142123616/f49797fb-1eeb-44dd-babf-e8050f341a7d)
In the first model, these were the recommended settings based on the output provided in the starter code. This set a badeline for me to determine how I might be able to optimize the model for future iterations. This model achieved an accuracy score of 73.10%
  
* What steps did you take in your attempts to increase model performance?
![nn2](https://github.com/morgantudor/deep-learning-challenge21/assets/142123616/e1d77464-40ff-4e13-9849-11457af9734a)
For my first optimization model, I wanted to test to see if the model was underfit by adding a third hidden layer. I added a third layer with 10 nodes. This model achieved a 73.01% accuracy.

![nn3](https://github.com/morgantudor/deep-learning-challenge21/assets/142123616/a5349409-b63b-42f1-9d86-0555b15f1197)
In the next model, I wanted to try having fewer nodes in the third layer and also try more binary activation functions so I switched all but the first layer to sigmoid activation functions. This model achieved a 73.14% accuracy rate.

![nn4](https://github.com/morgantudor/deep-learning-challenge21/assets/142123616/6f95216b-aa88-4d7e-a0a1-26195fd2b887)
In my final model, I wanted to keep 4 layers but test with less nodes to see if the data might be overfit. I tried 60, 30, 15, 5. This model achieved a 72.94% accuracy rate.

* Were you able to achieve the target model performance?
In the end, I was not able to achieve the target model performance. The closest I got was in my second optimization model with a rate of 73.14%.

##Summary
Overall, the most efficient model that I created was had an accuracy of 73.14%. This did not achieve the target model performance of 75% and would therefore mean that this model is not yet ready to be utilized as a trustworthy tool for this company. To increase the effectiveness of our model, many methods could be tried. I would recommend combing through the data in the preprocessing stage and removing more categories that may be too niche to generalize like "SPECIAL_CONSIDERATIONS". I might also consider reintroducing data like "NAME" as that might give the model more to work off of when classifying. 

