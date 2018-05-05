
### Clauses and Speedups(All the speed is the fastest among runs) : lud_omp.c
    1, 13: #pragma omp parallel for default(none) private(j,k,sum) shared(size,i,a)
       20: #pragma omp parallel for default(none) private(j,k,sum) shared(size,i,a)
       Parallel -- 147.242000 ms (num of threads = 8) , Serial -- 224.127000 ms
