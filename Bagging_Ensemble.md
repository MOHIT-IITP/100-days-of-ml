# [core idea]

[ "bootstraping" ] and [ "aggregation" ] -> together form BAGGING

- BOOTSTRAPING => you draw random sample from given population

  - in bootstraping har model alag data pe train hoga

  - if you are not able to capture the training data then it is high bias
  - training data pe result bad ->> high bias
  - training data pe result good ->> low bias
  - you model should given consistent result so low variance hona mangta
    We need [ LOW VARIANCE ] and [ LOW BIAS ]

- if you data have [ LOW BIAS , HIGH VARIANCE ] then go for [ BAGGING ]
- most use decesion tree as estimator in bagging

## step to do the bagging

- select base estimator (DECISION TREE , KNN, SVM)
- select number of estimator (you can change the number of tree)
- select max sample (how many row you want to give each model to train)
- Bootstrap use karna hai ya nhi
- how many features (like in ex they have 2 col , then they were use 2 col)
- bootstrap feature true or false

- [!tip] you will use random subspace and random batches when you have more number of col other wise you will you bagging for small number of col

- [!Note] bootstrap false sample without replacement
- [!note] n_jobs = -1 , then the work will be divided to the cpu and process will be faster

- [!tip] 37 % row ander hi reh jate hai bag me during the bagging process , that is why they are called OUT OF THE BOX CLASSIFIER

- Bagging tips
  - Bagging generally gives better results than Pasting
  - good results come around the 25% to 50% row sampling mark
  - random patches and subspaces should be used while dealing with high dimensional data
  - to find the correct hyperparameter values we can do GridSearchCV / RandomSearchCV
