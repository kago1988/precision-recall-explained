# precision-recall-explained
(Hobby) Here is an illustration on how to calculate **precision** and **recall** of a **trained classifier** on a **test data-set**. 
First, precision and recall on the test data-set are given by 

```
TP = apples, classified as apples 
TN = oranges, classified as oranges 
FP = oranges, classified as apples 
FN = apples, classified as oranges 
```

Here an example: 

Given a trained predictor f: input -> apple. I.e. a predictor, which always predicts "apple". 
We want to test the performance of this predictor on the following test data-set: 990 apples and 10 oranges. 

We have: 
```
TP = 990 
TN = 0 
FP = 10 
FN = 0

ACC = .99
PRE = 990 / (990 + 10) = .99 
REC = 990 / (990 + 0) = 1 
```

Our predictor would have a very high accuracy of 99%. A precision of 99%. And a recall of 100%. 
Precision can be seen as a measure of quality, and recall as a measure of quantity: 
**A system with high precision might leave some good items out, but what it returns is of high quality. 
A system with high recall might give you a lot of duds, but it also returns most of the good items.**
All in all, our predictor is really good for this test data-set. 

But as we all know, our test data-set is a bit biased. 
Precision and Recall can also help us find bias in the data-set. Consider the following calculation: 
We can calculate the "balanced accuracy" 
``` 
(SEN + SPE) / 2 
``` 
Where 
```
"sensitivity" = SEN = TP / P = 990 / 990 = 1 
```
and 
```
"specificity" = SPE = TN / N = 0 / 10 = 0. 
```
It follows: 
``` 
(SEN + SPE) / 2 = 0.5
``` 
which is- as it should be- not very high. 
