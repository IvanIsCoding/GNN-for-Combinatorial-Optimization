# GNNs for Solving Combinatorial Optimization Problems

![](https://raw.githubusercontent.com/amazon-science/co-with-gnns-example/955489d90df286ed9a29e939f364a7cad3706dd1/media/fig3_flowchart_v2.png)

| Notebook  | Open in Colab   | View Notebook| Related Paper |
|---|---| --- | --- |
| 00: GNNs for Solving Combinatorial Optimization Problems   | [![Notebook Viewer](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IvanIsCoding/GNN-for-Combinatorial-Optimization/blob/main/00_GNN_Definition.ipynb)  | [![nbviewer](https://img.shields.io/badge/view%20in-nbviewer-orange)](https://nbviewer.jupyter.org/github/IvanIsCoding/GNN-for-Combinatorial-Optimization/blob/main/00_GNN_Definition.ipynb) | [![arXiv](https://img.shields.io/badge/arXiv-2107.01188-b31b1b.svg)](https://arxiv.org/abs/2107.01188) |
| 01: GNNs versus Simulated Annealing for Max-Cut   | [![Notebook Viewer](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IvanIsCoding/GNN-for-Combinatorial-Optimization/blob/main/01_GNN_vs_SA_for_Max_Cut.ipynb)  | [![nbviewer](https://img.shields.io/badge/view%20in-nbviewer-orange)](https://nbviewer.jupyter.org/github/IvanIsCoding/GNN-for-Combinatorial-Optimization/blob/main/01_GNN_vs_SA_for_Max_Cut.ipynb) | [![arXiv](https://img.shields.io/badge/arXiv-2210.00623-b31b1b.svg)](https://arxiv.org/abs/2210.00623) |
| 02: GNNs versus Simulated Annealing for MIS   | [![Notebook Viewer](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IvanIsCoding/GNN-for-Combinatorial-Optimization/blob/main/02_GNN_vs_SA_for_MIS.ipynb)  |  [![nbviewer](https://img.shields.io/badge/view%20in-nbviewer-orange)](https://nbviewer.jupyter.org/github/IvanIsCoding/GNN-for-Combinatorial-Optimization/blob/main/02_GNN_vs_SA_for_MIS.ipynb) | [![arXiv](https://img.shields.io/badge/arXiv-2206.13211-b31b1b.svg)](https://arxiv.org/abs/2206.13211) |

Welcome to Graph Neural Networks (GNNs) for Solving Combinatorial Optimization Problems! In this series of Jupyter notebooks, we will investigate the paper [Combinatorial Optimization with Physics-Inspired Graph Neural Networks](https://arxiv.org/abs/2107.01188) by Schuetz et al.

We will implement the proposed architecture for the GNN using JAX + Flax and then replicate some results from the paper. Our Python code will solve Max-Cut and Maximum Independent Set instances on d-regular graphs of size up to 2000, which is neat!

After, we compare the results from the GNN against simulated annealing. This is related to two remarkable responses to the paper by Schuetz et al. The first is [Inability of a graph neural network heuristic to outperform greedy algorithms in solving combinatorial optimization problems like Max-Cut](https://arxiv.org/abs/2210.00623) by Boettcher. The second one is [Modern graph neural networks do worse than classical greedy algorithms in solving combinatorial optimization problems like maximum independent set
](https://arxiv.org/abs/2206.13211) by Angelini and Ricci-Tersenghi. These papers claim that the baseline used by Schuetz et al. was not adequate and that there are better algorithms out there. 

Can simulated annealing beat the neural networks? The answer is yes and we will discuss the implications for GNN architectures in the notebooks. The GNNs have strenghts and limitations and maybe Schuetz et al. downplayed the limitations a bit. Nevertheless, it is still an interesting paper and a fun one to implement.

## Code Structure

```
    .
    ????????? 00_GNN_Definition.ipynb            # Defines the GNN using JAX + Flax and PyQUBO
    ????????? 01_GNN_vs_SA_for_Max_Cut.ipynb     # GNNs vs OpenJij's SASampler on Max-Cut instances
    ????????? 02_GNN_vs_SA_for_MIS.ipynb         # GNNs vs OpenJij's SASampler on MIS instances
    ????????? gnn_for_co                         # Previous notebooks exported as a library by nbdev
    ????????? setup.py                           # installer generated by nbdev
    ????????? settings.ini                       # nbdev helper file specifying dependencies
    ????????? README.md                          # This file!
```

The code is written in Python using Jupyter Notebooks. Thanks to [nbdev](https://nbdev.fast.ai/), we export the notebooks as a Python library which allows us to reuse them in later notebooks or even in your machine. To install the `gnn_for_co` package defined in the notebooks, simply run:

```
pip install git+https://github.com/IvanIsCoding/GNN-for-Combinatorial-Optimization.git
```

## Related Code

Readers might also be interested in:

* [https://github.com/amazon-science/co-with-gnns-example](https://github.com/amazon-science/co-with-gnns-example): the official implementation by Schuetz et al. using PyTorch Geometric (also where we took the excellent diagram at the start of this README)
* [https://github.com/amazon-science/gcp-with-gnns-example](https://github.com/amazon-science/gcp-with-gnns-example): graph coloring with GNNs also by Schuetz et al.