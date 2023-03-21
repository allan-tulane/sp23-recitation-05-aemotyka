# CMPS 2200 Reciation 5
## Answers

**Name:** Jack Lehavi and Alex Motyka


Place all written answers from `recitation-06.md` here for easier grading.







- **1b.**
Random List
|    n |   qsort-fixed-pivot |   qsort-random-pivot |   tim-sort |   ssort |
|------|---------------------|----------------------|------------|---------|
|    1 |               0.002 |                0.000 |      0.003 |   0.004 |
|   10 |               0.015 |                0.022 |      0.002 |   0.010 |
|   50 |               0.068 |                0.096 |      0.003 |   0.093 |
|  100 |               0.173 |                0.237 |      0.009 |   0.342 |
|  200 |               0.396 |                0.517 |      0.022 |   3.283 |
|  300 |               1.216 |                1.211 |      0.029 |   3.089 |
|  500 |               1.454 |                1.422 |      0.047 |   8.541 |
|  700 |               1.789 |                2.773 |      0.089 |  22.144 |
|  850 |               2.340 |                2.645 |      0.111 |  54.490 |
| 1000 |               2.773 |                4.178 |      0.121 |  78.730 |

Sorted List
|    n |   qsort-fixed-pivot |   qsort-random-pivot |   tim-sort |   ssort |
|------|---------------------|----------------------|------------|---------|
|    1 |               0.001 |                0.000 |      0.002 |   0.005 |
|   10 |               0.023 |                0.026 |      0.001 |   0.010 |
|   50 |               0.264 |                0.100 |      0.002 |   0.080 |
|  100 |               1.136 |                0.204 |      0.003 |   0.262 |
|  200 |               5.033 |                0.530 |      0.004 |   1.102 |
|  300 |               8.209 |                0.863 |      0.006 |   2.190 |
|  500 |              74.076 |                1.319 |      0.010 |   5.862 |
|  700 |              95.154 |                2.329 |      0.021 |  12.652 |
|  850 |             178.731 |                2.535 |      0.018 |  17.765 |
| 1000 |             195.928 |                2.892 |      0.026 |  73.766 |

Selection sort runs in O(n^2). Quick sort fixed pivot and random pivot both run in O(nlogn) when the input is a random list. With a sorted list, quick sort with fixed pivot has a runtime of O(n^2) because it is running the worst case. The empirical running times in the tables all line up with these upper bound run times.

- **1c.**

|      n |   qsort-fixed-pivot |   qsort-random-pivot |   tim-sort |
|--------|---------------------|----------------------|------------|
|    100 |               0.001 |                0.006 |      0.003 |
|    200 |               0.001 |                0.003 |      0.005 |
|    500 |               0.000 |                0.002 |      0.007 |
|   1000 |               0.000 |                0.001 |      0.013 |
|   2000 |               0.001 |                0.001 |      0.027 |
|   5000 |               0.000 |                0.002 |      0.067 |
|  10000 |               0.001 |                0.003 |      0.125 |
|  20000 |               0.000 |                0.002 |      0.206 |
|  50000 |               0.001 |                0.005 |      0.898 |
| 100000 |               0.002 |                0.005 |     39.093 |

Clearly, the fastest sorting algorithm is qsort-fixed-pivot. Its runtime is significantly lower than tim-sort for every value of n, and remains very low while the runtime of tim-sort grows very large. However, the runtime of tim-sort would be significantly lower if the unsorted list contained "runs" of partially sorted values. Therefore, if the list is completely randomized, qsort is much more efficient, despite both qsort and timsort having worst-case runtimes of O(nlogn).