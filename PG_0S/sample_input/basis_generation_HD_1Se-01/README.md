# Description

Sample file `inout.txt` in this directory provides input for generating a very small ECG basis for the lowest $^1 S^e$ state of HD molecule. It starts from 0 basis functions and stops when the basis reaches 10 basis functions. When the basis size equals 5 and 10 functions, the program will save the input in separate files  
`inout_HD_1Se-01-00005.txt`  
`inout_HD_1Se-01-00010.txt`  
The calculation with this input file should take about 10 seconds on a single CPU core when double precision is used (gfortran compiler / Intel Core i9-7900X).
At the end of the calculation the energy should reproduce one decimal figure in the exact value of -1.165471922.

Note that the end value of the energy may differ slightly from one execution to another because each execution involves stochastic selection of the basis functions.  
