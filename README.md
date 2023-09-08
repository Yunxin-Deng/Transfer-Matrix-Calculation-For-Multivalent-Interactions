# Multivalent-Interactions-Calculation-Using-Transfer-Matrix

In this calculation, **the ligand has two binding domains** and **the target has multiple binding sites** that can be defined by users. The domain-site interaction energies and inter-domain cooperativity can be defined by userse also. The codes are separated to the first main section, which has the necessary functions to do transfer matrix calculation and followed four sections, which are corresponding to calculating four results in the main text of the [paper](https://www.sciencedirect.com/science/article/pii/S0006349522003162).

Any publication that discloses findings arising from using this source code should **cite the [paper](https://www.sciencedirect.com/science/article/pii/S0006349522003162)**. Please also refer to the Supplementary Information for a detailed description of the method. 

You can use the **online version** with this [Colab notebook](https://colab.research.google.com/drive/15Q1iayim6DeL17c8QIwhVgoEWL46ybcp#scrollTo=DXtCUhHG5Wc8).

To run the calculation, please follow the steps below.

1. Click **'Run cell'** of the **'Initializtion'** and **'Necessary functions'** cells first.
2. **Choose the sections** of results that the user would like to know. **Define the initial values** needed, such as the number of target sites, the domain-site interaction energies, etc. The energy values are in unit $k_BT$.
3. **Run all the cells in the chosen sections** and get the results.

## Sections of Results
1. The probabilities of unbound, single-domain bound and two-domain bound
2. The apparent binding affinity of ligand-target interaction
3. The apparent binding specificity of ligand-target interaction
4. Site-specific binding
### 1. The probabilities of unbound, single-domain bound and two-domain bound
* **Input values in 'Set values' section**:
  * Set number of target sites, $n$.  ('num_of_site = $n$')
  * Set domain-site interaction energies in $k_BT$ unit, $μ^A_i$ and $μ^B_i$.  ('A_site_energy = $μ^A_i$', 'B_site_energy = $μ^B_i$')
  * Set inter-domain cooperative energies in $k_BT$ unit, $μ^{AB}$ and $μ^{BA}$.  ('mu_AB = $μ^{AB}$', 'mu_BA = $μ^{BA}$')
  * Set the index of calculating concentration range in Molar unit. (e.g. *'c_lowest_index=-3'* and *'c_highest_index=0'* means the concentration calculated is from $10^{−3}$ M to $10^0$ M.
    
For example, setting the conditions: $n=3$, $μ^A_i=10 k_BT$ and $μ^B_i=5 k_BT$, $μ^{AB}=0 k_BT$ and $μ^{BA}=0 k_BT$, ligand concentration ranging from $10^{−13}$ M to $10^4$ M
```python
num_of_site = 3
A_site_energy = 10
B_site_energy = 5
mu_AB = 0 
mu_BA = 0 
c_lowest_index = -13
c_highest_index = 4
```
* **Run all cells below in this section**:
  * Set values 
  * Calculate probabilities of unbound, A bound, B bound and AB bound
  * Make plot
    
### 2. The apparent binding affinity of ligand-target interaction
* **Input values in 'Set values' section**:
  * Set number of target sites, $n$.  ('num_of_site = $n$')
  * Set domain-site interaction energies in $k_BT$ unit, $μ^A_i$ and $μ^B_i$.  ('A_site_energy = $μ^A_i$', 'B_site_energy = $μ^B_i$')
  * Set inter-domain cooperative energies in $k_BT$ unit, $μ^{AB}$ and $μ^{BA}$.  ('mu_AB = $μ^{AB}$', 'mu_BA = $μ^{BA}$')
  * Set the index of calculating concentration range in Molar unit. (e.g. *'c_lowest_index=-3'* and *'c_highest_index=0'* means the concentration calculated is from $10^{−3}$ M to $10^0$ M.
    
For example, setting the conditions: $n=10$, $μ^A_i=10 k_BT$ and $μ^B_i=5 k_BT$, $μ^{AB}=2 k_BT$ and $μ^{BA}=2 k_BT$, ligand concentration ranging from $10^{−10}$ M to $10^{-2}$ M
```python
num_of_site = 10
A_site_energy = 10
B_site_energy = 5
mu_AB = 2
mu_BA = 2 
c_lowest_index = -10
c_highest_index = -2
```
* **Run all cells below in this section**:
  * Set values 
  * Calculate the apparent affinity when the ligand has only A domain, only B domain or AB domains. (The result of affinity will be printed out.)
```python
Output: The apparent affinity of A-ligand is: 3.25 μM
        The apparent affinity of B-ligand is: 4.82e+02 μM
        The apparent affinity of AB-ligand is: 0.000857 μM
```
  * Make plot
    
### 3. The apparent binding specificity of ligand-target interaction
* **Input values in 'Set values' section**:
  * Set number of target sites, $n$.  ('num_of_site = $n$')
  * Set specific and non-specific domain-site interaction energies in $k_BT$ unit, $μ_s$ and $μ_n$.  ('specific_energy = $μ_s$', 'nonspe_energy = $μ_n$')
  * Set inter-domain cooperative energies in $k_BT$ unit, $μ^{AB}$ and $μ^{BA}$.  ('mu_AB = $μ^{AB}$', 'mu_BA = $μ^{BA}$')
  * Set the index of calculating concentration range in Molar unit. (e.g. *'c_lowest_index=-3'* and *'c_highest_index=0'* means the concentration calculated is from $10^{−3}$ M to $10^0$ M.
    
For example, setting the conditions: $n=4$, $μ_s=10 k_BT$ and $μ_n=5 k_BT$, $μ^{AB}=2 k_BT$ and $μ^{BA}=2 k_BT$, ligand concentration ranging from $10^{−13}$ M to $10^{-2}$ M
```python
num_of_site = 4
specific_energy = 10 
nonspe_energy = 5 
mu_AB = 2
mu_BA = 2
c_lowest_index = -13
c_highest_index = -2
```
* **Run all cells below in this section**:
  * Set values 
  * Calculate working concentration range and the apparent specificity of two-domain ligands. (The result of working concentration range and specificity of two-domain ligand will be printed out.)
```python
Output: The working concentration range is: 1.9267247677577812e-05 to 0.055242985057496065 uM
        The specificity range is: 10.14297448602567 to 13221.464309730512
```
  * Make plot
  * Calculate working concentration range and the apparent specificity of two-domain ligands. (The value and plotted figure of working concentration range and specificity of single domain ligand will be printed out.)
```python
Output: The working concentration range is: 8.58 to 1.8e+02 μM
        The specificity range is: 10.1 to 98.0
```
### 4. Site-specific binding

