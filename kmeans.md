### Clauses and Speedups(All the speed is the fastest among runs)
    1, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(static) reduction(+:delta)
       Parallel -- 1.562357s (num of threads = 8) , Serial -- 2.715432s

    2, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(static) reduction(+:delta)
       85:  #pragma omp parallel for private(i)
       Parallel -- 4.230084s (num of threads = 8) , Serial -- 2.715432s 

    3, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(static) reduction(+:delta)
       85:  #pragma omp parallel for private(i), shared(npts, pt, pts, nfeatures)
       Parallel -- 3.718231s (num of threads = 8) , Serial -- 2.715432s 
       
    4, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(static) reduction(+:delta)
       85:  #pragma omp parallel for private(i), shared(npts, pt, pts, nfeatures), reduction(min: max_dist)
       Parallel -- 4.308435s (num of threads = 8) , Serial -- 2.715432s 

    5, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(static) reduction(+:delta)
       108: #pragma parallel for reduction(+:ans), private(i), shared(numdims, pt1, pt2)
       Parallel -- 1.545632s (num of threads = 8) , Serial -- 2.715432s 
       
    6, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(guided) reduction(+:delta)
       Parallel -- 1.490168s (num of threads = 8) , Serial -- 2.715432s 
       
    7, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(dynamic) reduction(+:delta)
       Parallel -- 4.653307s (num of threads = 8) , Serial -- 2.715432s 
       
    8, 183: #pragma omp parallel shared(feature, clusters, membership, partial_new_centers, partial_new_centers_len)
       187: #pragma omp for private(i, j, index) firstprivate(npoints, nclusters, nfeatures) schedule(guided) reduction(+:delta)
       108: #pragma parallel for reduction(+:ans), private(i), shared(numdims, pt1, pt2)
       Parallel -- 1.442081s (num of threads = 8) , Serial -- 2.715432s
