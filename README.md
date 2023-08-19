# Introduction

TeraChem is general purpose quantum chemistry software designed to run on Nvidia CUDA-enabled GPU architectures under a 64-bit Linux operating system. Some of TeraChem features include:

1. Restricted, unrestricted, and restricted open shell Hartree-Fock and grid-based Kohn-Sham ground state energy and gradient calculations
2. Time-dependent density functional theory (TDDFT) and Configurational interaction singles (CIS) treatment of excited state energies
3. Full support of s, p and d-type atom-centered Gaussian basis functions, and effective core potentials with angular momentum of up to L=4.
4. Various DFT functionals, including range-corrected and Coulomb attenuated functionals (BLYP, B3LYP, PBE, PBE0, $$\omega$$PBE, $$\omega$$PBEh, $$\omega$$B97, $$\omega$$B97x, camB3LYP, etc) and DFT grids (800 - 80,000 grid points per atom)
5. Static grid (single grid used for the entire calculation) and dynamical grid (multigrid) integration.
6. Empirical dispersion correction (DFT-D3 and DFT-D2)
7. Polarizable Continuum Models for solvation
8. Geometry optimization (L-BFGS, Conjugate gradient, Steepest descent)
   1. The optimization can be carried out either in Cartesian or internal coordinates as specified in the start file (all input geometries are provided in Cartesians). The Cartesian->internal->   Cartesian coordinate transformation is performed automatically whenever required.
   2. Constrained optimization with frozen atoms, constrained bond lengths, angles, and dihedrals.
   3. Transition state search (Nudged elastic band) in internal and Cartesian coordinates
9. Ab initio molecular dynamics (NVE, NVT ensembles)
   1. Reversible Born-Oppenheimer dynamics
   2. Spherical boundary conditions
10. Support of multiple-GPU systems
11. Single/Dynamical/Double precision accuracy
12. QM/MM treatment of surrounding water molecules using [TIP3P ](#user-content-fn-1)[^1]force field
13. Natural bond orbital analysis through integration with [NBO6](https://nbo6.chem.wisc.edu/webnbo\_css.htm)
14. Polarizabilities for HF and closed-shell DFT methods
15. Runs on up to 16 GPUs in the same node in parallel, not parallelized to run on multiple nodes

[^1]: W. L. Jorgensen, J. Chandrasekha, J. D. Madura, R. W. Impey, and M. L. Klein, J. Chem. Phys. **79** 926 (1983)
