# precision-recall-explained
(Hobby) Here an illustration, how precision and recall is meant

In this illustration you can see how the precision and recall is being calculated. 

Precision and recall are relevant. Consider the following example: 

Given a trained predictor f: {orange, apple} -> orange. I.e. a predictor, which always predicts "apple". 
We want to test the performance of this predictor on the following test data-set: 990 apples and 10 oranges. 

We have: 
```
TP = 990 
FP = 10 
TN = 0 
FN = 0

ACC = .99
PRE = 990 / (990 + 10) = .99 
REC = 990 / (990 + 0) = 1 
```

Our predictor would have a very high accuracy of 99%. A precision of 99%. And a recall of 100%. 

In order to examine our test data-set for bias we can calculate the "balanced accuracy" 
``` 
(SEN + SPE) / 2 = 0.5
``` 
Where 
```
"sensitivity" = SEN = TP / P = .99 
```
and 
```
"specificity" = SPE = TN / N = .01. 
```
