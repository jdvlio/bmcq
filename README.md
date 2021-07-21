# bmcq

A simple (perhaps mundane) AWK script that adds up grades for multiple choice questions, 
the answers having been exported as a csv from Blackboard Learn.  Basically, it fixes 
what they should have done right in the first place.

# Description

This script is written to total marks based on a `.csv` file from the Blackboard
Learn "software suite". Its use is **limited to** assessments where all the
multiple choice questions were put in a *seperate* Blackboard test.

# Usage instructions

All the cases are the same so an example suffices.  Suppose the correct solution
is answering `(c)` for every question and there were 5 questions (it works for
arbitrarily large sets of multiple choice questions).  If this script is in
your current working directoy you run the following command:
```
 $ ./bmcq -v memo="ccccc"
```
# My (justified) rant

This serves as proof that we should not turn our backs on older software just
because we have newer, shinier things that are so convoluted that, at best,
they barely resemble a working solution.
