# bmcq

A simple (perhaps mundane) AWK script that adds up grades for multiple choice questions,
the answers having been exported as a `.csv` from Blackboard Learn.  Basically, it fixes
what should have been done right in the first place.

# Description

This script is written to total marks based on a `.csv` file from the Blackboard
Learn "software suite". CUrrently, use is limited to assessments where all the*
multiple choice questions were put in a **separate** Blackboard test.
Additionally, make sure that the "short" output is chosen.  This is done, when
exporting from BBL, to choose grouping by users only and **not also by question**.

# Usage instructions

If this script is in your current working directoy you simply run the following
command:
```
$ ./bmcq file.csv
```
__By default it prints to standard output__ so if you prefer to have the results
stored in a file, rather than dumped in your terminal, the following is sufficient:
```
$ ./bmcq file.csv > output.csv
```
Note that the output produced is itself also in `.csv` format as this is one of the few
formats understood by Blackboard Learn.

# Goals:

- [ ] Process multiple choice questions whose responses are arbitrary strings
- [ ] Have the responses be read from a file instead of as a cli argument

# My (somewhat justified) rant

This serves as proof that we should not turn our backs on older software just
because we have newer, shinier things that are so convoluted that, at best,
they barely resemble a working solution.

The old farts that made AWK really knew what they are doing and it is they who
are the true heroes of this tale!
