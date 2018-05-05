### Clauses and Speedups(All the speed is the fastest among runs, num of threads = 8) : euler3d_cpu.cpp
    1, 61: #pragma omp parallel for default(shared) schedule(static)
       110: #pragma omp parallel for default(shared) schedule(static)
       163: #pragma omp parallel for default(shared) schedule(static)
       194: #pragma omp parallel for default(shared) schedule(static)
       325: #pragma omp parallel for  default(shared) schedule(static) 
       Parallel: 7.10436s (fvcorr.domn.097K) ,  13.7019s (fvcorr.domn.193K), 21.3671s (missile.domn.0.2M)
       Serial:   87.8669s (fvcorr.domn.097K) ,  177.66s (fvcorr.domn.193K), 278.175s (missile.domn.0.2M)
