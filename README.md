# Hotel Cancellation Prediction
We will be using machine learning techniques to try to predict whether customers booking a hotel room will cancel or not to optimize hotel booking.

## Problem Framing
Our goal here is to identify whether a booking made by a customer will be cancelled or not. This classification will help in optimizing the room capacity. So if for example a customer is predicted to cancel their reservation, we can resell their room to another customer and therefore minimize the opportunity cost lost.

To do this, we will use Supervised Classification because we have a dataset defining which customers have cancelled (label) and from there we can train model to predict further data.

We will use F1-score as the main performance measure, which is a combination of Recall and Precision so that we can make sure that all the predicted cancel customers will actually cancel, and the model can predict all customers that will cancel.

The risks of wrong prediction will result in either opportunity cost lost if we incorrectly predicted that a customer will not cancel when they actually cancelled, or customer dissatisfaction when we predicted that a customer will cancel when in fact they did not cancel (so we don't have any room available for them, overbooking). This is a matter of Precision and Recall balance, and I think that it's best to prioritize Precision because a dissatisfied customer means they won't be coming back and they may give bad reviews which can damage our reputation in the long run. On the other hand, opportunity cost is a one-time cost that will not have any further damage to the company.

## Methodology
For this problem, we are going to be using multiple classification algorithms and choosing the best model to use for this problem.

## Result, Conclusion, and Recommendation
We were able to make a model that can predict whether a customer will cancel their booking with 83% accuracy, 81% precision, and 70% recall. This means that

Out of all the predicted cancel customers, we have a 81% confidence that all of them will actually cancel, and
We are confident that our prediction will cover 70% of all customers that will cancel.
From this prediction, we can make necessary adjustments on the number of rooms sold. When a customer book a room, we can run their information through this model and make a prediction whether they will cancel. If they are predicted to cancel, maybe we can resell their room to another customer so that there is no opportunity cost lost.

By using this model, we can also mitigate overbooking by only overselling when a customer is predicted to cancel, so there will be less dissatisfied customers.
