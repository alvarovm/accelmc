
### COMPILE WITH GCC
```
gcc -o mclj_npt mclj_npt.c -lm -lgsl -lgslcblas -lm
```


### COMPILE WITH GCC+ COMPILER OPTIMIZATION
```
gcc -O3 -o mclj_npt mclj_npt.c -lm -lgsl -lgslcblas -lm
```


### COMPULE WITH NVHPC
```
nvc -o mclj_npt mclj_npt.c -lm -lgsl -lgslcblas -lm
```

### COMPILE WITH GCC +OPENMP
```
gcc -fopenmp -o mclj_npt_omp mclj_npt.openmp.c -lm -lgsl -lgslcblas -lm -lgomp
```

### COMPULE WITH NVHPC+OPENACC
```
nvc -o mclj_npt_acc mclj_npt.acc.c -lm -lgsl -lgslcblas -lm
```

### SAMPLE RUN
```
time ./mclj_npt -N 10000 -rho .01 -nc 100 -dr 0.2 -seed 0 -ne 100
```

### COMPILE WITH GCC+GPROF, AND SAMPLE RUN
```
gcc -pg -o mclj_npt mclj_npt.c -lm -lgsl -lgslcblas -lm
time ./mclj_npt -N 3000 -rho .01 -nc 100 -dr 0.2 -seed 0 -ne 100
gprof ./mclj_npt gmon.out
```
