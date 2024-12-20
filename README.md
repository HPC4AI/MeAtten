# MeAtten
Optimizing Attention by Exploiting Data Reuse on ARM Multi-core CPUs.<br>

This paper was published in the Proceedings of the 38th ACM International Conference on Supercomputing (ICS '24), and you can find it [here](https://dl.acm.org/doi/10.1145/3650200.3656620). If you find our work beneficial to your research, we would greatly appreciate it if you could cite our paper and star the repository. Please feel free to contact us at fx_nudt@163.com if you have any questions.

# Abstract
Meatten is a high-performance self-attention operator library, with performance gains derived from operator fusion and multi-dimensional parallelization of the standard self-attention mechanism. It builds on fused micro-kernels and a new data layout suitable for SIMD vectorization. An analytic model is used to guide loop permutation, tiling, and batched parallelization according to the on-chip hierarchical memory architecture and workload characterization. 

# How to use
First, you need to install third-party libraries such as OpenBLAS and XNNPACK. Then,

```
cd csrc
make lib
cd ../benchmark/sdpa
make bench_meformer_sdpa.x
./run_bench_meformer_sdpa.sh
```

You may need to modify the installation paths of the third-party libraries in the Makefile.

# Platforms
![image](https://github.com/user-attachments/assets/543577f3-2e82-4836-bce9-c2d876777985)


# Performance

We apply MEATTEN to three representative ARM multi-cores against state-of-the-art libraries and compilers. Experimental results demonstrate that our approach consistently outperforms prior approaches across various evaluation scenarios and platforms.

![image](https://github.com/user-attachments/assets/d722c4ca-ecb7-4872-a948-f51eee2eaa94)


# Citation
```
@inproceedings{FuYDS24,
  title = {Optimizing Attention by Exploiting Data Reuse on ARM Multi-core CPUs},
  author = {Xiao Fu and Weiling Yang and Dezun Dong and Xing Su},
  year = {2024},
  doi = {10.1145/3650200.3656620},
  url = {https://doi.org/10.1145/3650200.3656620},
  pages = {137-149},
  booktitle = {Proceedings of the 38th ACM International Conference on Supercomputing, ICS 2024, Kyoto, Japan, June 4-7, 2024},
  publisher = {ACM},
}
```

# Acknowledge
[LibShalom](https://github.com/AnonymousYWL/LibShalom/blob/main/README.md)<br>
[FlashAttention 1](https://arxiv.org/abs/2205.14135)<br>
[FlashAttention 2](https://arxiv.org/abs/2307.08691)
