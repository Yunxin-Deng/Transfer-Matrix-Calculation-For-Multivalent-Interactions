# The probabilities of unbound, single-domain bound and two-domain bound
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
