# bmcq

A simple (perhaps mundane) AWK script that adds up grades for multiple choice questions,
the answers having been exported as a `.csv` from Blackboard Learn.  Basically, it fixes
what should have been done right in the first place.

# Description

This script is written to total marks based on a `.csv` file from the Blackboard
Learn "software suite". CUrrently, use is limited to assessments where all the*
multiple choice questions were put in a **separate** Blackboard test.

# Usage instructions

**Important note:** as this tool was created for mathematics students, and Blackboard's
*TeX* formatting is the stuff of nightmares, our "questions" were *PNG files which*
*contained the various possible answers.*  Hence, the choices presented by Blackboard
itself were simply `(a)` through `(e)`.  However, **see the "Goals" section below.**

All the cases are the same so an example suffices.  Suppose the correct solution
is answering `(c)` for every question and there were 5 questions (it works for
arbitrarily large sets of multiple choice questions).  If this script is in
your current working directoy you simply run the following command:
```
$ ./bmcq -v memo="ccccc" file.csv
```
__By default it prints to standard output__ so if you prefer to have the results
stored in a file, rather than dumped in your terminal, the following is sufficient:
```
$ ./bmcq -v memo="ccccc" file.csv > output.csv
```
Note that the output produced is itself also in `.csv` format as this is one of the few
formats understood by Blackboard Learn.

# Goals:

- [ ] Process multiple choice questions whose responses are arbitrary strings
- [ ] Have the responses be read from a file instead of as a cli argument

# My (somewhat justified) rant
<a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nd/4.0/">Creative Commons Attribution-NoDerivatives 4.0 International License</a>

This serves as proof that we should not turn our backs on older software just
because we have newer, shinier things that are so convoluted that, at best,
they barely resemble a working solution.

The old farts that made AWK really knew what they are doing and it is they who
are the true heroes of this tale!
