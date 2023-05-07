# Stocks_forecasting_Stacked_LSTM
Forecasting stocks using Stacked LSTM model.



Project Name: Stocks Forecasting using stacked LSTM-RNN models:


Phases of the Project:

A. Collection of Stocks data(any stock) from any source.
-> Here We will use the pandas_datareader and from it we will use the TIINGO platform's API system
-> the stocks being forecasted here are stocks of AAPL

B. Preprocessing the data.
-> We select the Close price column of the stock to process and predict it.
-> Since we will be using the stacked LSTM model, and LSTM is very sensitive to the scale of data, we will scale down the data using a 
minMax Scaler.
-> Lastly, we will split the data into training and testing data.
** Since, this is a time-series data we will use appropriate steps to process the data

C. Model Creation and Training:

C(1): Model Creation:
-> for the model we will use 3 layers of LSTM each with 100 neuron or nodes
   -> the first LSTM layer will be the input layer so we will set it accordingly
-> Using Dropouts is optional.
-> adding the dense layer with 1 neuron since a regression problem statement
-> optimizer selected is: Adam ; Loss function is: Mean Squared Error(MSE)

C(2): Model Training:
-> the model in this case is trained for 100 epochs with batch_size being 64


C(3): Evaluating the model performance:
**Note: Use Inverse Transformation on the scaled down data or the MSE would be senseless.

-> after inverse transformation the MSE is calculated on the training data and testing data:
  * mse_on_training_data: 219.6089  (During the run of the project and the time of creation of this report)
  * mse_on_testing_data: 151.416186 (""   "" ""    """  """ """ " "")

D. Visualising the performance:
**note: this phase is all about being creative

-> here we will plot the graph using simple logics.
  -> Plot the main data, over it plot the training data using look_backs and same for the testing data.
