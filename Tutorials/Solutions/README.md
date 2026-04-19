# ODW solution repo

This directory contains encrypted solutions to the quizzes and challenges on this repo.
To be able to see the solutions, you need a secret key.
With it, run the following command to produce all solutions.

```
$ gpg -d solutions.tar.gz.gpg | tar -xvzf -
```
to produce all solutions.

The structure is the same than the `Tutorials` folder.

To add a new solution, or edit an existing solution. First, unpack the solutions as above. Edit and run the notebook (check that it is up-to-date with it's blank counterpart). Then, run
```
$ tar -czvf - 01_Accessing_Open_Data/ 02_Generating_Waveforms/ 03_Signal_Processing/ 04_Searches/ 05_Parameter_Estimation/ | gpg -c > solutions.tar.gz.gpg
```
Then finally git add the `solutions.tar.gz.gpg` and commit in the usual way.

