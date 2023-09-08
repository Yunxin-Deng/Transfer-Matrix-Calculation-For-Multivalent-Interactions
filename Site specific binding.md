# Site specific binding
* **Input values in 'Set values' section**:
  * Set number of target sites, $n$.  ('num_of_site = $n$')
  * Set domain-site interaction energies between ligand domain and nonspecific site on target in $k_BT$ unit, $μ^A_n$ and $μ^B_n$.  ('A_site_energy = $μ^A_n$', 'B_site_energy = $μ^B_n$')
  * Set inter-domain cooperative energies in $k_BT$ unit, $μ^{AB}$ and $μ^{BA}$.  ('mu_AB = $μ^{AB}$', 'mu_BA = $μ^{BA}$')
  * Set the index of calculating concentration range in Molar unit. (e.g. *'c_lowest_index=-3'* and *'c_highest_index=0'* means the concentration calculated is from $10^{−3}$ M to $10^0$ M.
    
For example, setting the conditions: $n=10$, $μ^A_n=10 k_BT$ and $μ^B_n=0 k_BT$, $μ^{AB}=0 k_BT$ and $μ^{BA}=0 k_BT$, ligand concentration ranging from $10^{−13}$ M to $10^0$ M
```python
num_of_site = 10
A_site_energy = 10
B_site_energy = 0
mu_AB = 0 
mu_BA = 0 
c_lowest_index = -13
c_highest_index = 0
```
* **Choose the specific domain and specific site index $j$**:
  * Choose the specific domain. (Input 'A', 'B' or 'None')
  * Choose the specific site position, $i$. ($i<=n$)
  * Set domain-site interaction energies between the ligand domain that recognize the specific site and the specific site of target in $k_BT$ unit, e.g. $μ^B_s$.

For example, setting the conditions: the specific domain is domain B, the site is the $5^{th}$ site, $\mu^B_s=8k_BT$
```python
domain = "B"
site = 5
changed_energy = 8
```
* **Run all cells below in this section**:
  * Set values 
  * Choose the specific domain and specific site index $j$
  * Calculate the working concentration range of the ligand with one specific and one nonspecific domain. (The result of working concentration range to recognize specific site will be printed out.)
```python
Output: The working concentration range is: 0.0077 to 0.0493 μM
```
  * Make plot of **specific and nonspecific site binding probabilities** under different ligand concentrations.
  * Make plot of binding probabilities of each site **under certain ligand concentration**. (The concentration is **chosen by the user in Molar unit**. For example, if the user wants the ligand concentration to be $10^{-7}$ M, $c=10^{-7}$ M, the variable *'def_c_index'* should be '-7' as shown in python code below in this cell.)
```python
def_c_index = -7
```
  * The result of single-domain ligand with the specific domain for comparison. (The value and plotted figure of working concentration range with single specific domain ligand will be printed out.)
```python
Output: The working concentration range is: 3.4e+02 to 1.11e+05 μM
```
  * Make plot of single-domain ligand binding probabilities of each site under certain ligand concentration. (The concentration is **chosen by the user in Molar unit**. For example, if the user wants the ligand concentration to be $10^{0}$ M, $c=10^{0}$ M, the variable *'def_c_index'* should be '0' as shown in python code below in this cell.)
```python
def_c_index = 0
```
