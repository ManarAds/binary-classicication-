This project demonstrates a binary classifier built using a simple linear model with a sign-based decision function. The classifier is designed to learn its weights from data through a hinge-loss optimization process.

Implementation Steps
Binary Classifier Definition:

Implements a classifier with methods:
getScore: Calculates the score 
𝑤
1
⋅
𝑥
1
+
𝑤
2
⋅
𝑥
2
w 
1
​
 ⋅x 
1
​
 +w 
2
​
 ⋅x 
2
​
  for input features.
getLabel: Derives the label by applying the sign function on the score.
predict: Predicts a label based on input features using getScore and getLabel.
Prediction Verification:

verbosePrediction: Prints the predicted label, target label, and a correctness check for each input, aiding in visualizing classification performance on training data.
Margin Calculation:

Computes the margin as 
(
𝑤
1
⋅
𝑥
1
+
𝑤
2
⋅
𝑥
2
)
⋅
𝑦
(w 
1
​
 ⋅x 
1
​
 +w 
2
​
 ⋅x 
2
​
 )⋅y, showing the agreement between prediction and target label.
Hinge Loss:

Implements getHingeLoss to compute the Hinge Loss for predictions, which penalizes incorrect or borderline predictions. The gap parameter defines the margin requirement for correctly classified points.
Weight Update Rule:

Implements a train method to adjust weights based on Hinge Loss. The update rule is applied iteratively to improve classification accuracy, moving the decision boundary closer to correctly classifying the data.
