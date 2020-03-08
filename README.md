# binary-classifiers-identify-Numbers-
Identify the number from 1 - 10 by using binary classifier.
![input](https://github.com/LadyWinterD/binary-classifiers-identify-Numbers-/blob/master/Numbers.PNG?raw=true)
1, firstly model i built is SGDClassifier (recall and precision measure)
output:
i used SGDClassifier for my first model,measuring accuracy using cross-validation: 
96% accracy on all cross-validation folds

2, confusion matrix
recall and precision measure.   
recision accuracy: %83 
recall accuracy : 
![output](https://github.com/LadyWinterD/binary-classifiers-identify-Numbers-/blob/master/OUTPUT.PNG?raw=true)

I used to 2 ways to train my model.
* one way is to create a system that can classify the digit images into 10 class is train 10 binary classifiers, one foe each digit. then if i want to classify an image, i can get the decision secor from each classifier for that image and you select the class whose classifier outputs the highest score. it is called ONE-VERSUS-THE REST(OvR) strategy, also called one versus all.
*another strategy is to train a binary classifier for every pair of digits: one to distinguish 0 and 1, another to distinguish 0 and 2, another for 1 and 2 and so on. it is called the **one-versus-one(OvO)strategy. if there are N calsses, you need to train N × (N – 1) / 2 classifiers. if i need to classify an image, i have to run the image through all 45 classifiers and see which class wins the most duels. the main advantage of OvO is each classifier only need to be trained on the part of the training set for the 2 classes.

![output](https://github.com/LadyWinterD/binary-classifiers-identify-Numbers-/blob/master/Numbers.PNG)

