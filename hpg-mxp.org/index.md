
# High Performance Generalized Minimal Residual - Mixed-Precision (HPG-MxP) Benchmark #

Ichitaro Yamazaki, Jennifer Loe, Christian Glusa, Sivasankaran Rajamanickam
Piotr Luszczek, and Jack Dongarra

## Introduction ##

HPG-MxP is a software package that performs a fixed number of multigrid preconditioned
(using a Gauss-Seidel smoother) Generalized minimal residual (PGMRES) iterations.

The HPG-MxP rating is a weighted GFLOP/s (billion floating-point operations per
second) value that is composed of the operations performed in the PGMRES
iteration phase over the time taken to finish the solve.  The overheads such as
the time of problem construction and any structural modifications to improve
the final performance are amortized over several iterations (the amortization
weight) and added to the runtime.

Integer arrays describing the original problem structure have global and local
scope (the global indices are unique across the entire distributed memory
system, while the local indices are unique only within a single memory image of
a single MPI rank).  Integer data for global/local indices have three modes:

* 32/32 - global and local integers are 32-bit entities
* 64/32 - global integers are 64-bit, local are 32-bit
* 64/64 - global and local integers are 64-bit entities

These various modes are required in order to address sufficiently big problems
if the range of indexing exceeds value of 2 to power 31 (roughly 2.1B), or to
conserve storage costs if the range of indexing is less than 2 to power 31.

The HPG-MxP software package requires the availibility on your system of an
implementation of the  Message Passing Interface (MPI) if  MPI build of HPG-MxP
was enabled at configuration time, and a compiler that supports OpenMP pragma
syntax.  An implementation compliant with MPI version 1.1 is sufficient.

## Valid Runs ##

HPG-MxP can be run in just a few minutes from start to finish.  However, official
runs must be at least 1800 seconds (30 minutes) as reported in the output file.
The Quick Path option is an exception for machines that are in production mode.
In this situation, which should be confirmed by sending a note to the HPG-MxP
Benchmark authors, the Quick Path option can be invoked by setting the run time
parameter equal to 0 (zero).

A valid run must also execute a problem size that is large enough so that data
arrays accessed in the GMRES iteration loop do not fit in the cache of the device
in a way that would be unrealistic in a real application setting.  At present, this
restriction means that the problem size should be large enough to occupy a
significant fraction of the *main memory*, or at least 1/4 of the total.

Future memory system architectures may require restatement of the specific memory
size requirements.  But the guiding principle will always be that the problem
size should reflect what would be reasonable for a real sparse iterative solver.

## Documentation ##

The source code documentation can be generated with a Doxygen (version 1.8 or
newer).
