# The apparent binding affinity of ligand-target interaction
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
    
