# Neural_Network_Charity_Analysis

# PURPOSE:

### The purpose of this project is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

#### The CSV file contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

  - **EIN and NAME** — Identification columns
  - **APPLICATION_TYPE** — Alphabet Soup application type
  - **AFFILIATION** — Affiliated sector of industry
  - **CLASSIFICATION** — Government organization classification
  - **USE_CASE** — Use case for funding
  - **ORGANIZATION** — Organization type
  - **STATUS** — Active status
  - **INCOME_AMT** — Income classification
  - **SPECIAL_CONSIDERATIONS** — Special consideration for application
  - **ASK_AMT** — Funding amount requested
  - **IS_SUCCESSFUL** — Was the money used effectively


# RESULTS:

### Data Preprocessing

What variable(s) are considered the target(s) for your model? 
- **_'IS_SUCCESSFUL'_** field

What variable(s) are considered to be the features for your model? - 
- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE

What variable(s) are neither targets nor features, and should be removed from the input data?
- EIN
- NAME
- USE CASE
- ORGANIZATION
- INCOME_AMT

### Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
- hidden_nodes_layer1 = 8
- hidden_nodes_layer2 = 3
- number_input_features = 48

Were you able to achieve the target model performance?
- The accuracy of this model is at 72.94% which is less than the desired 75%

What steps did you take to try and increase model performance?
- Tried 4 other models after changing the neurons and the accuracy of these was still less than the desired target.
- As a next step, three other features were dropped and reran the model with various neurons and activation functions. However, the accuracy was still not over 75%. 

Details of these models are listed below.

- Sample dataframe is as below:

![orig_df](https://user-images.githubusercontent.com/74985818/125155455-fed3bf80-e12d-11eb-9e66-acc49f60432c.png)

- 'EID' & 'NAME' columns were dropped as they did show high significance in this analysis.

![drop2](https://user-images.githubusercontent.com/74985818/125155474-2fb3f480-e12e-11eb-8a52-c0c41c7507f9.png)

- Using One Hot Encoder, the remaining categorical columns have been transformed to numberical values.

![onehot](https://user-images.githubusercontent.com/74985818/125155493-55d99480-e12e-11eb-9677-651b607de990.png)

- The final DF has been split into features and targets and then split intp training and test datasets

![split_conv](https://user-images.githubusercontent.com/74985818/125155530-90433180-e12e-11eb-877c-8e7ba73fb1ac.png)

- Initial Neural Network Model used and it's accuracy:

![model1](https://user-images.githubusercontent.com/74985818/125155584-00ea4e00-e12f-11eb-97f1-6fd15c8a5e80.png)

![model1_acc](https://user-images.githubusercontent.com/74985818/125155587-08115c00-e12f-11eb-9c84-6e6896a21714.png)


### Various Trails used to get the accuracy above the required 75% mark.

#### Trial 1 Model & Accuracy

![trial1](https://user-images.githubusercontent.com/74985818/125155594-1495b480-e12f-11eb-89c4-bec6b9f1e0f8.png)
![trial1_acc](https://user-images.githubusercontent.com/74985818/125155595-152e4b00-e12f-11eb-8ca9-6d3ef782ca4a.png)

#### Trial 2 Model & Accuracy

![trial2](https://user-images.githubusercontent.com/74985818/125155596-152e4b00-e12f-11eb-8047-a2c0db20e58f.png)
![trial2_acc](https://user-images.githubusercontent.com/74985818/125155598-152e4b00-e12f-11eb-988f-1b03d7483f61.png)

#### Trial 3 Model & Accuracy

![trial3](https://user-images.githubusercontent.com/74985818/125155599-15c6e180-e12f-11eb-8dad-8ef49b06e1c6.png)
![trial3_acc](https://user-images.githubusercontent.com/74985818/125155600-15c6e180-e12f-11eb-81fd-e34eb9ceef35.png)

#### Trial 4 Model & Accuracy

![trial4](https://user-images.githubusercontent.com/74985818/125155601-15c6e180-e12f-11eb-9f9f-b2d6db596d97.png)
![trial4_acc](https://user-images.githubusercontent.com/74985818/125155602-15c6e180-e12f-11eb-8ef9-14184de249ac.png)

### For the next few models, three other columns noisy columns, 'USE CASE', 'ORGANIZATION', 'INCOME_AMT' are dropped.

![drop4](https://user-images.githubusercontent.com/74985818/125155697-a9001700-e12f-11eb-91ff-a1a0e72a6206.png)

#### Trial 5 Model & Accuracy

![trial5](https://user-images.githubusercontent.com/74985818/125155603-15c6e180-e12f-11eb-87b1-c08c6a1f5f4b.png)
![trial5_acc](https://user-images.githubusercontent.com/74985818/125155604-165f7800-e12f-11eb-97f6-e948d837feca.png)

#### Trial 6 Model & Accuracy

![trial6](https://user-images.githubusercontent.com/74985818/125155605-165f7800-e12f-11eb-8cd6-c35ef678ecb3.png)
![trial6_acc](https://user-images.githubusercontent.com/74985818/125155607-165f7800-e12f-11eb-8cd2-344613b3eda4.png)

#### Trial 7 Model & Accuracy

![trial7](https://user-images.githubusercontent.com/74985818/125155608-165f7800-e12f-11eb-97c3-1a0a76d87265.png)
![trial7_acc](https://user-images.githubusercontent.com/74985818/125155609-16f80e80-e12f-11eb-8f39-899ab45f1945.png)

#### Trial 8 Model & Accuracy

![trial8](https://user-images.githubusercontent.com/74985818/125155610-16f80e80-e12f-11eb-9677-68f34cb5b2d8.png)
![trial8_acc](https://user-images.githubusercontent.com/74985818/125155611-16f80e80-e12f-11eb-8e3b-8e48aac9593c.png)


# SUMMARY:

A total of 9 Neural Network models have been implemented and the highest accuracy that could have been obrtaine is 73.06%
- Initial Model: Params: 465; Loss: 55.24%; Accuracy: 72.94%
- Trial Model 1: Params: 433; Loss: 55.39%; Accuracy: 73.00%
- **Trial Model 2: Params: 2281; Loss: 55.05%; Accuracy: 73.06%**
- Trial Model 3: Params: 4801; Loss: 55.14%; Accuracy: 72.94%
- Trial Model 4: Params: 7351; Loss: 55.10%; Accuracy: 72.92%
- Trial Model 5: Params: 289; Loss: 57.00%; Accuracy: 72.44%
- Trial Model 6: Params: 1741; Loss: 57.09%; Accuracy: 72.33%
- Trial Model 7: Params: 3901; Loss: 56.84%; Accuracy: 72.41%
- Trial Model 8: Params: 6451; Loss: 56.74%; Accuracy: 72.40%

Way ahead: More noisy variables can be dropped and try various other combinations of activation functions with higher epochs could result in a better score.

HDF5 files for all the above models are saved at every 5 epochs in the ![Challenge](https://github.com/MamidalaV/Neural_Network_Charity_Analysis/tree/main/Challenge) folder.
