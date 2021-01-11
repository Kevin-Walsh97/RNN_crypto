# RNN_crypto
 
 ## Introduction

 Initially, neither one of the models performed all that well. While the first model, the one that used previous crypto prices to predict futures ones, heavily outperformed the other, it was really a demonstration in mediocrity. To try and improve the performance of each of the models, I played around with the drop rate as well as the batch sizes. However, my main method for improving performance for each of the models was to increase the windows from 10 days to 20 days. As I will highlight below, this did little to change the initial conclusions. 

 ## Which Model had a Lower Loss? 

 The closing price model clearly outperformed the FNG model in terms of loss. Although it is not nearly as smooth as we might have liked, the loss plot does have the traditional 'hockey stick' shape that we have come to know that indicates that as the model iterates through (again and again) the data, its loss improves, in that it decreases. While the FNG loss plot does trend downward (somewhat) it is extremely jagged. This is to the point where it is inconclusive if loss is improving overtime. 

 ## Which Model's Predictions Tracked Actual Values Better?

 Again, the closing price model was clearly the better of the two in this respect. Although its predictions does not mirror the real values as close as we have seen, the model does follow the same basic trend of the real values. In terms of FNG model, the predictions do not follow the real values **at all**. In this respect, it might be said that the FNG value is not a good predictor of future values

 ## Which Window Size Worked Best For the Model? 

 The difference between 10 days and 20 days was minimal. I saw some improvement when toying around with batch_size for the price model, but saw no material change in the FNG model despite change several parameters of the model.