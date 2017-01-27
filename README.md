# Titanic-Keras
Using ANNs with Keras for the Titanic Survival Prediction Dataset

This dataset was given in a Kaggle competition: 

https://www.kaggle.com/c/titanic

where, given some passenger data the algorithm will predict who will die and who will survive
by using some ML algorithms.

In this case, a dense (fully-connected) ANN with two hidden frames was used. Survival
is treated as a binary variable: 0 if dead and 1 if survived.

Input:

Train.csv

    PassengerId - a number giving the unique ID of the passenger
    Survived - survival (0 = No, 1 = Yes)
    Pclass - passenger class (1 to 3)
    Name - passenger full name
    Sex - male or female
    Age - age of the passenger
    SibSp - number of siblings or spouses on board 
    Parch - number of parents or children on board
    Ticket - ticket number
    Fare - ticket fare
    Cabin - (if applicable) cabin in the ship
    Embarked - port of embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)

Test.csv

    Same as Train.csv, but no Survived column
    
Output:

result.csv

    PassengerId - a number giving the unique ID of the passenger. Should be the same as Test.csv
    Survived - survival (0 = No, 1 = Yes)
    
Features used were PClass (since first class was prioritized when boarding), sex (females were embarked first)
and Parch (kids were also prioritized).

This got 77.9% accuracy in the kaggle Test set.
