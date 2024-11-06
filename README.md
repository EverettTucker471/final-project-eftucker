# final-project-eftucker

### Milestone 3 Work

## Progress
- I first parsed the data from the provided CSVs and cleaned some of the times to convert them to absolute times from epoch.
- Next, I seperated the data by type of connection, and removed some unnessesary features from the data
- Then, I graphed some of the time series to look at their mean and variance graphically. This showed that a lot of the data was distributed vairly randomly, but I proceeded to make sure that there weren't any discernable correlations.
- I next ran a linear model to analyze the correlation between Signal Strength, Data Throughput, and Latency for each time stamp. This linear model showed no discernable correlation, suggesting a more complex relationship or random data.
- Then I plotted some lag plots showing how the different times series (Signal Strength, Data Throughput...) changed over time. This also showed that there weren't any real patterns within the lag plots.
- To analyze the data more, I chose to use an autoregressive Multi-Layer Perceptron to predict the Data Throughput from the previous Data Throughput values. This model is similar to the data that I will have access to in the field, so it is good for a final model.
- To help train the autoregressive MLP model, I used GridSearchCV to optimize the parameters for solver, activation function, and alpha value. Furthermore, I also adjusted the buffer size to determine how much of a window to use for prediction.
- The MLP model concluded that there was no discerable correlation between the data, and the correlation coefficient tended towards 0, which suggests that the input data was random.

## Future Work
- In the future, I want to try some more of the data sets in my sampled data. It appears that the signal data was perhaps distributed randomly, or is too difficult to predict by traditional methods.
- I believe that the methodology of the autoregressive MLP algorithm is promising for these types of time series predictions. However, I need to find data that has a more discernable pattern, or perhaps reframe the basis of my prediction to more a moving average approach.

Goal: To predict future mobile throughput from previous time series data
