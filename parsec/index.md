
# Parallel Runtime Scheduling and Execution Controller

PaRSEC is a generic framework for architecture aware scheduling and management of micro-tasks on distributed many-core heterogeneous architectures. Target applications or algorithms will be expressed as a Direct Acyclic Graph of tasks with labeled edges designating data dependencies. DAGs are represented in a compact problem-size independent format that can be queried on-demand to discover data dependencies in a totally distributed fashion. PaRSEC assigns computation threads to the cores, overlaps communications and computations and uses a dynamic, fully-distributed scheduler based on architectural features such as NUMA nodes and algorithmic features such as data reuse.

The PaRSEC Environment provides a software ecosystem composed of a runtime component to dynamically execute task-based applications on heterogeneous distributed systems, and a productivity toolbox that comprises a development framework for the support of multiple Domain Specific Languages (DSLs) and extensions, with debugging, trace collection, and analysis tools.

## DPLASMA: Distributed Parallel Linear Algebra Software for Multicore Architectures

<a title="flyer" href="https://icl.utk.edu/graphics/posters/files/SC13-DPLASMA.pdf" target="_blank">DPLASMA</a> is the leading implementation of a dense linear algebra package for distributed heterogeneous systems. It is designed to deliver sustained performance for distributed systems where each node featuring multiple sockets of multicore processors, and if available, accelerators like GPUs or Intel Xeon Phi. DPLASMA achieves this objective through the state of the art PaRSEC runtime, porting the Parallel Linear Algebra Software for Multicore Architectures (PLASMA) algorithms to the distributed memory realm.

DPLASMA's feature set includes:

* Linear systems of equations (Cholesky, LU [inc. pivoting, PP], LDL [prototype]).
* Least squares (QR &amp; LQ).
* Symmetric eigenvalue problem (Reduction to Band [prototype]).
* Level 3 Tile BLAS (GEMM, TRSM, TRMM, HEMM/SYMM, HERK/SYRK, HER2K/SYR2k.
* Covers double real, double complex, single real, and single complex (D, Z, S, C) precisions.
* Provides ScaLAPACK-compatible interface for matrices in F77 column-major layout
* Supports: Linux, Windows, Mac OS X, UN*X (depends on MPI, hwloc)

## Additional Information

For more information feel free to look at the different sources of documentation the project offers: online documentation, README, public&nbsp;<a title="Wiki" href="https://bitbucket.org/icldistcomp/parsec/wiki/Home" target="_blank">wiki</a>&nbsp;and/or our <a href="https://www.icl.utk.edu/publications?f%5Bsearch%5D=parsec">publications using the PaRSEC runtime</a>. Two moderated mailing-lists are available, one for <a href="https://groups.google.com/a/icl.utk.edu/d/forum/dplasma-users">users</a> and one for <a title="Devel" href="https://groups.google.com/a/icl.utk.edu/d/forum/dplasma-devel" target="_blank">developers</a>. Feel free to join us.

When referencing PaRSEC in a publication please use the following reference&nbsp;<a style="font-size: 11px; line-height: 21px;" href="http://www.icl.utk.edu/node/616">DAGuE: A Generic Distributed DAG Engine for High Performance Computing</a>&nbsp;(<a href="http://www.icl.utk.edu/publications/export/bibtex/616">bibtex</a>)

<a href="https://scan.coverity.com/projects/41"> <img src="https://scan.coverity.com/projects/41/badge.svg" alt="Coverity Scan Build Status" /> </a>


## Latest PaRSEC News

<span class="NewsDate-Alt">2017-09-26</span>
<div class="NewsHeadline-sm"><a href="news/news.html%3Fid=378.html">PaRSEC tutorials</a></div>
<br />
<span class="NewsDate-Alt">2015-12-04</span>
<div class="NewsHeadline-sm"><a href="news/news.html%3Fid=371.html">PaRSEC development branches are now public </a></div>
<br />
<span class="NewsDate-Alt">2015-12-01</span>
<div class="NewsHeadline-sm"><a href="news/news.html%3Fid=370.html">PaRSEC 2.0.0-rc2 released</a></div>
<br />
<span class="NewsDate-Alt">2015-06-08</span>
<div class="NewsHeadline-sm"><a href="news/news.html%3Fid=364.html">PaRSEC 2.0.0-rc1 released</a></div>
<br />
<span class="NewsDate-Alt">2014-04-15</span>
<div class="NewsHeadline-sm"><a href="news/news.html%3Fid=340.html">PaRSEC / DPLASMA 1.2.1 is up and running !</a></div>

