# Random Forest
Random forest algorithm is a supervised classification algorithm. As the name suggest, this algorithm creates the forest 
with a number of trees. 

If you know the decision tree algorithm. You might be thinking are we creating more number of decision trees and how can we 
create more number of decision trees. As all the calculation of nodes selection will be same for the same dataset. :open_mouth:

Yes. You are true. Same dataset is used every time. But we introduce randomness in order to decide which feature to pick 
while splitting.

If you are not aware of the concepts of decision tree classifier, Please spend some time. There is no alternative of 
spending time :stuck_out_tongue:

### Random Forest Training Pseudocode

```python
def train_random_forest(num_of_nodes, num_of_trees):
  for n in range(num_of_trees):
    for l in range(num_of_nodes - 1):
      Randomly select “k” features from total “m” features where k << m
      Among the “k” features, calculate the node “d” using the best split point
      Split the node into daughter nodes using the best split.
```
This will give you `n` independent decision trees which will be ensembled at the time of predictions.


### Random Forest Prediction Pseudocode

```python
def predict_random_forest(trees, input_x):
  targets = []
  for tree in trees:
    # Takes the test features and use the rules of each randomly created decision tree to predict the 
    # outcome and stores the predicted outcome (target)
    target = tree.predict(input_x)
    targets.append(target)
  # Calculate the votes for each predicted target
  votes = collections.Counter(targets)
  # Consider the high voted predicted target as the final prediction from the random forest algorithm.
  return votes.most_common()
```
