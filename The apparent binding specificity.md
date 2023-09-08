# The apparent binding specificity of ligand-target interaction
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
