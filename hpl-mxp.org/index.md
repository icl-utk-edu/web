
# HPL-MxP Mixed-Precision Benchmark

The HPL-MxP benchmark seeks to highlight the emerging convergence of
high-performance computing (HPC) and artificial intelligence (AI) workloads.
While traditional HPC focused on simulation runs for modeling phenomena in
physics, chemistry, biology, and so on, the mathematical models that drive
these computations require, for the most part, 64-bit accuracy. On the other
hand, the machine learning methods that fuel advances in AI achieve desired
results at 32-bit and even lower floating-point precision formats. This lesser
demand for accuracy fueled a resurgence of interest in new hardware platforms
that deliver a mix of unprecedented performance levels and energy savings to
achieve the classification and recognition fidelity afforded by higher-accuracy
formats.

HPL-MxP strives to unite these two realms by delivering a blend of modern
algorithms and contemporary hardware while simultaneously connecting to the
solver formulation of the decades-old HPL framework of benchmarking the largest
supercomputing installations in the world. The solver method of choice is a
combination of LU factorization and iterative refinement performed afterwards
to bring the solution back to 64-bit accuracy. The innovation of HPL-MxP lies in
dropping the requirement of 64-bit computation throughout the entire solution
process and instead opting for low-precision (likely 16-bit) accuracy for LU,
and a sophisticated iteration to recover the accuracy lost in factorization.
The iterative method guaranteed to be numerically stable is the generalized
minimal residual method (GMRES), which uses application of the L and U factors
to serve as a preconditioner. The combination of these algorithms is
demonstrably sufficient for high accuracy and may be implemented in a way that
takes advantage of the current and upcoming devices for accelerating AI
workloads.

