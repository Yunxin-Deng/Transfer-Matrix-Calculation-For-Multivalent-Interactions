# Transfer-Matrix-Calculation-For-Multivalent-Interactions

In this calculation, **the ligand has two binding domains** and **the target has multiple binding sites** that can be defined by users. The domain-site interaction energies and inter-domain cooperativity can be defined by userse also. The codes are separated to the first main section, which has the necessary functions to do transfer matrix calculation and followed four sections, which are corresponding to calculating four results in the main text of the [paper](https://www.sciencedirect.com/science/article/pii/S0006349522003162).

Any publication that discloses findings arising from using this source code should cite the [paper](https://www.sciencedirect.com/science/article/pii/S0006349522003162). Please also refer to the Supplementary Information for a detailed description of the method. 

You can use the online version with this [Colab notebook](https://colab.research.google.com/drive/15Q1iayim6DeL17c8QIwhVgoEWL46ybcp#scrollTo=DXtCUhHG5Wc8).

To run the calculation, please follow the steps below.

1. Click **'Run cell'** of the **'Initializtion'** and **'Necessary functions'** cells first.
2. **Choose the sections** of results that the user would like to know. **Define the initial values** needed, such as the number of target sites, the domain-site interaction energies, etc. The energy values are in unit $k_BT$.
3. **Run all the cells in the chosen sections** and get the results.
