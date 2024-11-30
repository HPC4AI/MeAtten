# MeAtten
Optimizing Attention by Exploiting Data Reuse on ARM Multi-core CPUs.<br>
The paper was published at the Proceedings of the 38th ACM International Conference on Supercomputing (ICS 24) and you can find it via the [link](https://dl.acm.org/doi/10.1145/3650200.3656620). If you find our work helpful to your research, we would greatly appreciate it if you could cite our work and star the repository.

# Abstract
We present MEATTEN, a memory-efficient attention fusion scheme and batched approach to exploit ARM multi-core CPUs effectively. It builds on fused micro-kernels and a new data layout suitable for SIMD vectorization. An analytic model is used to guide loop permutation, tiling, and batched parallelization according to the on-chip hierarchical memory architecture and workload characterization. We apply MEATTEN to three representative ARM multi-cores against state-of-the-art libraries and compilers. Experimental results demonstrate that our approach consistently outperforms prior approaches across various evaluation scenarios and platforms.

# How to install

# How to use

# Performance

Just run `MeAtten/benchmark/sdpa/run_bench_meformer_sdpa.sh`.

If you have any questions, please contact fx_nudt@163.com. Thanks.
