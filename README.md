# nhl-prediction-notebooks
Predict NHL hockey player seasonal performance

## Introduction
Fantasy hockey drafting relies on predicting how well the players could perform
in the future. This model use hockey players' performance in the previous seasons
to predict their performance in the next season. This model used data from the
NHL stats API. It considered the players' seasonal performance statistics as well
as that of the teams. The data was split into training and testing groups by players.
To train the model, the data was sliced into overlapping windows of 4 seasons. 
The model was trained to predict the statistics for the last season from previous
3 seasons. A deep neural network is used to make the prediction. The targets
are performance statistics that important for fantasy hockey points. For skaters,
their goals, assits and shots were predicted. For goalies, their saves, team wins
and goals against were predicted.

## Results
The prediction results for the next season is shared on a website 
[https://nhl-projection.herokuapp.com/](https://nhl-projection.herokuapp.com/).
The users could define custome rules to calculate the fantasy scores.
The players could be searched by their names, teams or positions.

As for the performance of the models. For the model for skaters, the R<sup>2</sup>
on the test set is 0.68 and it is 0.46 for the model for goalies. 
The following figure plotted an example predicted results for all the 
players in season 20192020.
![prediction](https://user-images.githubusercontent.com/24282911/140999295-af89ea47-9933-4f19-8c1e-53774d90b26d.png)
