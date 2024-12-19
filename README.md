# Analysis #

## Overview ## 
- The purpose of the analysis is to help Alphabet Soup to develop a tool to help predict whether an applicant will be able to receive funding based on the dataset provided, by using deep learning and machine learning techniques. 

## Results ##

### Data Preprocessing ###

- Target Variable: IS_SUCCESSFULL
--IS_SUCCESSFUL represents whether funding to an organization was used effectively


- Features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS INCOME_AMT, ASK_AMT_binned
-- ASK_AMT column was binned and categorized into low, medium, high, and very high funding ranges. 

- Removed Variables: EIN, NAME, SPECIAL_CONSIDERATIONS
-- EIN and NAME do not contribute to the predictive model because they are unique identifiers.
-- SPECIAL_CONSIDERATIONS was determined to add little value because it mostly had "N".

### Compiling, Training, and Evaluating the Model ###

- Input features
-- 77 input features was used in the model. The layers and the neuron numbers were chose to help reduce dimensionality progressively and help the models training efficiency. 
- Neurons and Layers
-- First Hidden Layer: 16 neurons, ReLU activation
-- Second Hidden Layer: 8 neurons, ReLU activation
-- Third Hidden Layer: 4 neurons, ReLU activation
--Output Layer: 1 neuron, Sigmoid activation 

- Target Performance
-- I was unable to achieve the targe model performance after three attempts. 
-- Validation Accuracy: ~72.58%
--Final Validation Loss: ~0.5575


- Steps taken to include model performance
-- The third layer was added after the first attempt 
-- ASK_AMT was binned for second attempt
-- Epoch number was increased for third attempt to 400 

## Summary ##
- The highest validation achieved was at 72.25% which is not enough to indicate exceptional predictive power. 
- Recommendations
-- Collecting more data or enriching the dataset with other external information like industry benchmarks. 
-- Engineering features from the existing data to identify more relationships, and most important predictors
-- Trying alternative methods such as Random Forest or Gradient Boosting