### Clauses and Speedups
    1, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(static) reduction(+:delta)
       Serial -- 2.715432s,   Parallel -- 1.562357s (num of threads = 8)
