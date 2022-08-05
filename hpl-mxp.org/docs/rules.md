
Rules
=====

The idea for the benchmark is to solve a system of linear equations to 64-bit
floating point accuracy by (a) doing a mixed-precision factorization of a matrix
and computing an approximate solution from the low-precision factorization (LU
decomposition), and then (b) use an iterative method (like GMRES) in 64-bit precision
to iterate with the approximate low-precision solution to compute a final
solution and obtain the accuracy one would have achieved by LU decomposition in
64-bit floating point arithmetic. The low-precision LU factors should be used
as a preconditioner in the iterative algorithm.

The benchmark should use the
[HPL benchmark harness](https://www.netlib.org/benchmark/hpl/) with a modification of the matrix
generator. The modified generator should produce a non-symmetric matrix with the diagonal
entries being the sum of the row's off-diagonal elements, this will force the matrix to
be diagonally dominant.

In an attempt to obtain uniformity across all computers in performance
reporting, the algorithm used in solving the low-precision system of equations
in the benchmark procedure must numerically conform to an LU factorization. In
particular, the operation count for the algorithm must be
2/3n^3 + O(n^2)
floating point operations even though double-precision arithmetic is not
required.

The HPL harness computes a backward-error:
||Ax-b\||\_oo / (||A||\_oo ||x||\_oo + ||b||\_oo) / (N * Epsilon),
where Epsilon is the machine precision in 64-bit
floating point arithmetic (on IEEE machines this is 1/2^53) and
N is the size of the problem. There is no restriction on the problem
size N. However, if the backward-error is greater than 16, the run
is invalid.

The implementation is allowed to do balancing and scaling to obtain the numbers
within range of the floating point format, but the time required for balancing
must be included in the time to solution.

The factorization can use mixed precision during its construction, e.g., the
panel factorization and triangular solves can be done in 32-bit arithmetic and
the Schur complement (matrix-matrix multiplication of the form
A[2,2] <- A[2,2] - A[2,1] * inverse(A[1,1]) * A[1,2]
can be computed in 16-bit arithmetic with 32-bit accumulation.

The computation rate is based on the time to solve the problem: factor the
matrix in lower precision, perhaps balance the matrix to prevent overflow,
perform GMRES, or another iterative method, in 64-bit floating point arithmetic using the LU factors as a
preconditioner. If the implementation takes more than 50 iterations, the method
should trigger a failure and the run is invalid.

In computing a rate of execution, 2/3 n^3 + 3/2 n^2 operations
(the formula 2/3 n^3 - 1/2 n^2
accounts for LU factorization and 2\*n^2 for the subsequent back- and
forward-solves) will be divided by the total time-to-solution to arrive
at the rate of operations per second.

As part of the submission of results we expect the submitter to provide a
detailed explanation of the algorithm used in the submission.

We have provided a reference implementation the purpose of which is to show how the
benchmark could be implemented. We do not expect this to be used when
running of the benchmark. Optimizations should be applied to achieve higher
performance than the reference implementation could achieve. The
[reference implementation](https://bitbucket.org/icl/hpl-ai/) can be found on Bitbucket.
