# deep--learning-challenge

Overview:
The purpose of this analysis to review data provided by the charity Alphabet Soup and create a tool that can assist in predicting if a future application has a good chance of success and therefore is a good candidate for funding.
Results:
Data Preprocessing:
The success or failure of past projects is the target that we are aiming to predict for future projects.
In addition to the success of the past projects, we are also given the following information on each project:
•	EIN and NAME—Identification columns
•	APPLICATION_TYPE—Alphabet Soup application type
•	AFFILIATION—Affiliated sector of industry
•	CLASSIFICATION—Government organization classification
•	USE_CASE—Use case for funding
•	ORGANIZATION—Organization type
•	STATUS—Active status
•	INCOME_AMT—Income classification
•	SPECIAL_CONSIDERATIONS—Special considerations for application
•	ASK_AMT—Funding amount requested
•	IS_SUCCESSFUL—Was the money used effectively
The EIN and NAME of the project were removed from the features list as they will not have an impact on the success of the project. 
Compiling, Training, and Evaluating the Model:
The fist round of using a neural network to predict outcomes was using 16 units for two hidden layers, both with relu activations and the sigmoid activation for the output layer. This achieved a 72% accuracy. I then created a new optimization file where the data was further processed and the neural network settings were adjusted.
The data contains many outliers in the amount asked column. 23.93% of the data was more that 1.5 STD from the interquartile range. Adjustments were attempted at 2 STDs, and 2 STDs from the interquartile range to see if that would eliminate less than 20% of the data or have a big impact on the accuracy of the neural network model and after multiple attempts the traditional 1.5 STDs was accepted as the optimum cut off. 
All attempts at different settings of the neural network used the amount of columns in the dataframe as the input dimensions. Different activations and unit amounts were experimented with as well as different amount of layers. The highest accuracy achieved was with 32 units and relu activation for both the first and second hidden layers and a sigmoid activation for the output layer.



