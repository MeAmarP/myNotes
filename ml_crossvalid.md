### K-fold vs. Monte Carlo cross-validation
---
#### k -Fold Cross Validation:
Suppose you have 100 data points. For k-fold cross validation, these 100 points are divided into k equal sized and mutually-exclusive 'folds'. For k=10, you might assign points 1-10 to fold #1, 11-20 to fold #2, and so on, finishing by assigning points 91-100 to fold #10. Next, we select one fold to act as the test set, and use the remaining k−1 folds to form the training data. For the first run, you might use points 1-10 as the test set and 11-100 as the training set. The next run would then use points 11-20 as the test set and train on points 1-10 plus 21-100, and so forth, until each fold is used once as the test set.

#### Monte-Carlo Cross Validation:
Monte Carlo works somewhat differently. You randomly select (without replacement) some fraction of your data to form the training set, and then assign the rest of the points to the test set. This process is then repeated multiple times, generating (at random) new training and test partitions each time. For example, suppose you chose to use 10% of your data as test data. Then your test set on rep #1 might be points 64, 90, 63, 42, 65, 49, 10, 64, 96, and 48. On the next run, your test set might be 90, 60, 23, 67, 16, 78, 42, 17, 73, and 26. Since the partitions are done independently for each run, the same point can appear in the test set multiple times, which is the major difference between Monte Carlo and cross validation.

#### Comparison:
Each method has its own advantages and disadvantages. Under cross validation, each point gets tested exactly once, which seems fair. However, cross-validation only explores a few of the possible ways that your data could have been partitioned. Monte Carlo lets you explore somewhat more possible partitions, though you're unlikely to get all of them--there are (10050)≈1028 possible ways to 50/50 split a 100 data point set(!).

If you're attempting to do inference (i.e., statistically compare two algorithms), averaging the results of a k-fold cross validation run gets you a (nearly) unbiased estimate of the algorithm's performance, but with high variance (as you'd expect from having only 5 or 10 data points). Since you can, in principle, run it for as long as you want/can afford, Monte Carlo cross validation can give you a less variable, but more biased estimate.

Some approaches fuse the two, as in the 5x2 cross validation (see Dietterich (1998) for the idea, though I think there have been some further improvements since then), or by correcting for the bias (e.g., Nadeau and Bengio, 2003).

#### Refer:
https://stats.stackexchange.com/questions/51416/k-fold-vs-monte-carlo-cross-validation