# precision-recall-explained
(Hobby) Here is an illustration on how to calculate precision and recall of a **trained classifier**. 
First, precision and recall are on the test data-set are given by the formulas 

```
TP = apples, classified as apples 
TN = oranges, classified as oranges 
FP = oranges, classified as apples 
FN = apples, classified as oranges 
```

Here an example: 

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
Precision can be seen as a measure of quality, and recall as a measure of quantity. So our predictor is really good for this test data-set. 

But as we all know, our test data-set is a bit biased. 
Precision and Recall can also help us find bias in the data-set. Consider the following calculation: 
We can calculate the "balanced accuracy" 
``` 
(SEN + SPE) / 2 = 0.5
``` 
Where 
```
"sensitivity" = SEN = TP / P = 990 / 990 = 1 
```
and 
```
"specificity" = SPE = TN / N = 0 / 10 = 0 
```
