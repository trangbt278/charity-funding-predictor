# charity-funding-predictor

1. **Overview** of the analysis: 
Create a model to predicting whether applicants will be successful if funded by Alphabet Soup.

2. **Results**: 

  * Data Preprocessing
    * The column "IS_SUCCESFUL" is considered the target of the model
	* The columns "EIN" and "NAME" are not used for the train or test for the model. And also the data with Status is 0 (inactive) is not used for the model. Those data is removed out of the input for the model
    * The remaining of columns in the input data after using get_dummies() are consider features of the model

  * Compiling, Training, and Evaluating the Model
    * The first run
	- 3 layers (the first with 80 units and relu activation, the second with 30 units and relu activation and the output layer with 1 unites and sigmoid activation)
	- perform 100 epochs
	- result: Loss: 0.5525644071665171, Accuracy: 0.7259474992752075
    * The second run -  adjust input data
	- remove data with inactive status and create bins for AFFILIATION and INCOME_AMT and increase values in each bins
	- use the same model with  the first one: 3 layers (the first with 80 units and relu activation, the second with 30 units and relu activation and the output layer with 1 unites and sigmoid activation)
	- perform 100 epochs
	- result is  a litte better Loss: Loss: 0.5572488729300854, Accuracy: 0.7267319560050964
    * The third run - Increase number of neurons 
	- 3 layers (the first with 100 units and relu activation, the second with 60 units and relu activation and the output layer with 1 unites and sigmoid activation)
	- perform 100 epochs
	- result: Loss: 0.5591464170854576, Accuracy: 0.7266153693199158
    * The forth run -  add more layes
	- 4 layers (the first with 80 units and relu activation, the second with 30 units and relu activation and the thrid with 30 units and relu activationand the output layer with 1 unites and sigmoid activation)
	- perform 150 epochs
	- result: it got worse Loss: 0.6955428924042222, Accuracy: 0.532306969165802
	
    * After 4 attempts, it didnt get to target performance. I will do more on adjust the data and add more neurons
	

3. **Summary**: 
