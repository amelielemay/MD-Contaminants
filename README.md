# Molecular Dynamics Simulation Input Files for Organic Contaminants in LAMMPS
<img width="1413" alt="picture2" src="https://user-images.githubusercontent.com/79615161/211542940-fa37831e-b1fb-45ea-a4e6-5c3c9ddb6b7b.png">

### A broad range of organic compounds
#### Introduction

This library contains input files for 82 organic compounds, spanning those categorized as legacy contaminants (benzene, formaldehyde) to emerging contaminants (PFASs, pyrethroid pesticides) as well as pharmaceutical products (aspirin, ibuprofen) and compounds naturally present in the environment (acetic acid, isoprene). The molecules were constructed using the OPLS-AA model<sup>1</sup>, which represents the potential energy of a simulated system as a sum of semi-empirical non-bonded pairwise interactions (Van der Waals, Coulomb) and bonded interactions (bond stretching, angle bending, torsion). This library accompanies our publication<sup>2</sup> in which we modeled the compounds at the water-air interface.

Other potential applications of our input files include simulations of organic compounds in soils (to determine soil partition coefficients), in octanol-water or phospholipid bilyaer systems (to determine properties relevant to toxicity), or on synthetic adsorbents (to develop advanced water treatment materials). We ask that you cite our publication if you use any of our compound files in your work.

### Instructions for Use

#### File Setup
Each compound folder contains 2 files.
```
example.lj
```
The above file lists the atoms, bonds, angles, and dihedrals of the molecule.

```
control01
```
The above file lists the interaction parameters for each atom type. Upon execution it reads the example.lj file and runs a short simulation of the compound in the canonical (NVT) ensemble.

#### Details on Compound Structures

Compounds that carry ionizable groups were modeled in their protonation state at pH 7. For instance, PFOA is modeled as deprotonated (no H atom on its hydroxyl group).

For combinations of moieties for which parameters do not exist in the OPLS-AA database, the closest approximations or substitutions were employed. Any approximations or substitutions are listed in the comments of the compound .lj file.

### Authors
This database was created by the following members of the [Interfacial Water Group](http://bourg.princeton.edu/) at Princeton University:

Amélie Lemay, Ethan Sontarp, Daniela Martinez, Philip Maruri, Raneem Mohammed, Ryan Neapole, Morgan Wiese, Jennifer A.R. Willemsen, Ian C. Bourg

Please contact Amélie Lemay (alemay@princeton.edu) with questions or corrections to this database.


![princeton](https://user-images.githubusercontent.com/79615161/211543436-6be71659-6485-4ef5-be93-7c6bf1181330.png)


### License

Shield<sup>3</sup>: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

We ask that you please cite our publication<sup>2</sup> if you use these files in your work. 

### References and Attributions

1. Jorgensen, W. L.; Maxwell, D. S.; Tirado-Rives, J. Development and testing of the OPLS all-atom force field on conformational energetics and properties of organic liquids. *J. Am. Chem. Soc.* 1996, 118, 11225-11236.
2. 2. Lemay, A.C., Sontarp, E.J., Martinez, D., Maruri, P., Mohammed, R., Neapole, R., Wiese, M., Willemsen, J.A.R., Bourg, I.C. Molecular Dynamics Simulation Prediction of the Partitioning Constants (K<sub>H</sub>, K<sub>iw</sub>, K<sub>ia</sub>) of 82 Legacy and Emerging Organic Contaminants at the Water-Air Interface. *Environ. Sci. Technol.* 2023, 57(15), 6296-6308.
3. The license description in our README.md and accompanying LICENSE.md file were obtained from the Github repository [cc-licenses by santisoler](https://github.com/santisoler/cc-licenses). 

### Acknowledgment
This research was supported by the National Science Foundation (NSF) Environmental Engineering Program and the High Meadows Environmental Institute (HMEI) Summer Internship Program at Princeton University. MD simulations were performed using resources of the National Energy Research Scientific Computing Center (NERSC) and the Princeton Institute for Computational Science and Engineering (PICSciE).
