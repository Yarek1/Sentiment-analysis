# Sentiment-analysis
This project is about analysis of cellphones and accessories reviews.
Firstly load data from amazon datasets, there are no NA values.
After first look we can see time is in Unix type, but change to universal time.
(Unix time (also known as Epoch time, POSIX time,[1] seconds since the Epoch,[2] or UNIX Epoch time[3]) is a system for describing a point in time.
It is the number of seconds that have elapsed since the Unix epoch, minus leap seconds; the Unix epoch is 00:00:00 UTC on 1 January 1970.)
Most of reviews is positive and write in between 2005-2009 year.

After first look and preprocessing, data was used to recommendation analysis. Not only review score is important, also amount of reviews is too.
It's because review can have score 5, but have only one opinion. Importance of review is check by ratio of likes to likes+dislikes.

In next part is analysis of amount of words in review and most used words in opinion. From the set of words in all opinions I removed "stopwords".
This is collection of 100 most used words in english language. It can be import from nltk library.

At the end there is comparision of accuaracy of logistic regression solvers:
LIBLINEAR – A Library for Large Linear Classification SAG- Minimizing Finite Sums with the 
Stochastic Average Gradient SAGA- A Fast Incremental Gradient Method With Support for Non-Strongly Convex Composite Objectives
For small datasets, ‘liblinear’ is a good choice, whereas ‘sag’ and ‘saga’ are faster for large ones.
For multiclass problems, only ‘newton-cg’, ‘sag’, ‘saga’ and ‘lbfgs’ handle multinomial loss; ‘liblinear’ is limited to one-versus-rest schemes.
‘newton-cg’, ‘lbfgs’, ‘sag’ and ‘saga’ handle L2 or no penalty ‘liblinear’ and ‘saga’ also handle L1 penalty
‘saga’ also supports ‘elasticnet’ penalty ‘liblinear’ does not support setting penalty='none'.
