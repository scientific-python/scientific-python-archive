# Scientific Python Sparse Summit - Meeting 1

Monday September 26th, 2022 --- 11AM - 12PM PST

## Presentations

### 1. Proposal for array semantics in `scipy.sparse`
- Dan Schult - professor of mathematics at Colgate university
- Grant proposal to CZI: introduce sparse array semantics to `scipy.sparse` package
- A scipy.sparse array "frontend" on top of existing sparse implementation in scipy
- Grant submitted to CZI for cycle 5
- One of the first features: a 1-D sparse container
  * First step towards moving away from matrix (must be 2D)
- Developing a transition plan for scipy.sparse for matrix -> array interface
  * Important consideration for transition plan: input from downstream/consumer libraries
  * Ecosystem coordination documents (SPEC) to formalize ideas

### 2. Pydata-sparse current and future work
- Hameer Abbasi - Future of pydata/sparse
- Have/had a GSoC student working on this
- Optimality w/ simplicity
  * Avoid temporaries
  * Avoid unnecessary iteration
  * No pointer chasing
  * No optimal scheduling
- Simplicity
  * Can use numpy incantation to achieve sparse results (not yet working, but WIP)
    - Has been done in the C++/dense world (e.g. `xtensor`)
    - and sparse world (e.g. TACO)
- Requires codegen at runtime
  * maybe a compiler at runtime
    - If so, options exist `cpppy`
      * Limitations of cpppy - no wheels/conda for windows
  * Another option: LLVM codegen
- hameerabbasi/xsparse
- Gitter

### 3. Needs/roles of sparse in GraphBLAS
- Jim Kitchen: GraphBLAS
- GraphBLAS - solving graph problems with sparse linear algebra
- Bindings for many languages
- Low-level Graphblas spec which underlies a C implementation and higher-level implementations/wrappers
- GraphBLAS features
  * Missing is never 0
  * semirings (e.g plus-times, min-plus)
  * masking
  * Internal sparse formats (CSR, CSC, dense versions)
  * Zero-copy interface to numpy
  * Parallelism - openMP implementation of matrix operations
- Benchmarks:
  - Takeaway - 20x speedup even over scipy.sparse implementation of pagerank
  - Highly tuned for graph fns
### 4. Needs/roles of sparse in scverse
- Isaac Virshup - scverse
  * Collections of packages for analysis of single-cell data
- single-cell data: high-throughput assay
  * Millions of observations, 10k+ metrics
- Why sparse?
  * 20k possible genes, usually 3-5k counts per cell
  * ~90% sparse
  * Increasing dataset size (1m+)
  * Sparse necessary for storage, memory usage, and compute time
- Normal workflow:
  * data->UMAP->clustering: graph-based
- Moving towards spatial transcriptomics
  * Spatial graphs
  * Graphlearning, e.g. pytorch-geometric
- How is sparse data handled now?
  * A: [`anndata`](https://anndata.readthedocs.io/en/latest/) - specialization of `xarray`
  * HDF5 or Zarr backends
- What does `scverse` want?
  * Array semantics
  * Support for xarray
  * Work with dask
  * consistency throughout the ecosystem (e.g. work with scikit-learn)
  * Out-of-core sparse arrays (e.g. graphblas binary format)
  
- More genomics
  * sparse adjacency representations
  * Billions of events on a 3bil x 3bil
  * Similar to `anndata`
  * out-of-core support very important


### 5. Needs/roles of sparse in scikit-learn
- Overview of formats and how they are used
- Sandwich product
- Generalized matrix-matrix
- Options, each with pros and cons
    - Do eveyrything ourselves in Cython, but maintenance complexity
    - Use SciPy
    - tabmat
- Needs: API conformity (NumPy/SciPy), efficient multi-threaded sparse matrix ops (preferably with C/C++ interface)

## Discussion

Please feel free to add discussion topics here during the BoF session. For example, if you want to discuss a point raised during the pydata-sparse BoF:

- [name=rossbar]: I'd like to discuss XXX re: pydata-sparse

---

- CJ Carey - scipy.sparse maintainer (by chance, not choice :) )
  * Reasonable representation of non-graph-based use-cases
  * Sparse matrices for speed, obvious use-case
  * Another use-case: dealing with datasets that don't fit in RAM
  * Tradeoffs when considering native code implementations
    - It would be very convenient to only use one datatype for indices and one for data
    - In practice, users might want flexibility (e.g. uint8 for indices)
  * scipy.sparse wants to support as much as possible, within reason
    - Handle special cases/very tight performance/memory-focused implementations in downstream libraries

- Erik Welch: Comprehensive benchmarks would be useful across projects

- Isaac Virshup: how reasonable is it to have multiple implementations
  * CJ: Currently kind-of support different sparse formats/memory layouts; therefore multiple backends shouldn't be too difficult
  * Caveat - sparse methods are delegated based on format w/ autoconversion of formats when a match isn't found
- Isaac: scientific Python ecosystem is still working on supporting dense operations on different array types, so how reasonable is it for sparse arrays?
  * CJ: depends on what subset of the array API you need to support - 10 most common operations are easy/already supported - more niche cases maybe not so much
  * sparse is a bit more tabula rosa

- Jarrod: Zarr & xarray as backends
  * xarray can't use scipy.sparse because scipy.sparse doesn't support array protocols (yet)
  * Could anyone say more about Zarr?
  * Isaac: will be discussing with Zarr whether the concept of offsets into the Zarr format
  * Nezar: HDF5 was the first backend (dense interface, but implement sparse format e.g. CSR)
    - Can access sparse arrays in cloud currently via kerchunk (sp?)
    - Is Zarr willing to support sparse natively
  * Hameer: tabular data would likely be straightforward to support
    - In pydata-sparse/xsparse: we recognize it's not possible to codegen everything; have to do some things on the fly (including types, formats)
  * CJ: Agreed - this is necessary for maximum performance; however, this is a limitation for scipy because scipy needs to work without a cpp compiler
    - This is why a sparse API is probably the way forward - suppoort multiple implementations

- Jim: Re: priorities - how important is ndimensional vs. getting 1D/2D working
  * Jarrod: scientific-python - focus on 1D/2D first: major goal is to get rid of matrix semantics in favor of array semantics
  * Sparsity along only certain dimensions - potentially more exotic formats
    - Hameer: Can have different representations for different dimensions depending on sparsity needs (e.g. dict-like along one dimension, ptr-based along another)
      * TACO has identified some of these needs
    - Erik: talk to me before adopting TACO (I think it's more complicated than it needs to be)
      * https://github.com/GraphBLAS/binsparse-specification/ 

- At this summit, graph applications are very represented - want to get a feel for the landscape of applications for sparse

- Jarrod: Plans for followup
  * General agreement for multiple implementations, API would be a goal
    - Design/communicate API via scientific Python SPEC

- Future meeting planning
  * Ross + Isaac will coordinate
  * Think about backend folks, e.g. Zarr. Also xarray - nice perspectives to have for future summits
  * Try to keep this general timeslot - multiple possible weeks

- Hameer - xsparse development time potentially freeing up in within the next few months

- Stefan: For next meeting - I'd like to learn more about formats for higher-dimensional data
  * Good material out there - will link to it
      * https://arxiv.org/abs/1804.10112
      * https://www.youtube.com/watch?v=sQOq3Ci4tB0
  * Erik: I can present "why not TACO"
      * See some TACO formats visualized here: https://nbviewer.org/github/GraphBLAS/binsparse-specification/blob/main/sparsetensorviz/notebooks/Example_Rank4-taco.ipynb