# Citing TeraChem

Any published work that utilizes TeraChem shall include the following references:&#x20;

* I.S. Ufimtsev and T. J. Martínez, “Quantum Chemistry on Graphical Processing Units. 3. Analytical Energy Gradients and First Principles Molecular Dynamics,” J. Chem. Theo. Comp., 2009, 5, p2619.
* A. V. Titov, I. S. Ufimtsev, N. Luehr, and T. J. Martínez, “Generating Efficient Quantum Chemistry Codes for Novel Architectures,” J. Chem. Theo. Comp., 2013, 9, p213.

Additionally, there are certain modules of the code that should be referenced when used:

* Effective Core Potentials: C. Song, L.-P. Wang, and T. J. Martínez, “Automated Code Engine for Graphical Processing Units: Application the Effective Core Potential Integrals and Gradients,” J. Chem. Theo. Comp., 2016, 12, p92.
* Time-dependent Density Functional Theory (TDDFT): “Excited-State Electronic Structure with Configuration Interaction Singles and Tamm-Dancoff Time-Dependent Density Functional Theory on Graphical Processing Units,” J. Chem. Theo. Comp., 2011, 7, p1814.
* Polarizable Continuum Models (PCM): “Quantum Chemistry for Solvated Molecules on Graphical Processing Units Using Polarizable Continuum Models,” J. Chem. Theo. Comp., 2015, 11, p3131.&#x20;
* Hole-hole Tamm-Dancoff approximated (hh-TDA) DFT: C. Bannwarth, J. K. Yu, E. G. Hohenstein, T. J. Martínez, “Hole-hole Tamm-Dancoff-approximated density functional theory: a highly efficient electronic structure method incorporating dynamic and static correlation” J. Chem. Phys., (2020), accepted; ChemRxiv DOI: 10.26434/chemrxiv.11828256.

TeraChem benefits from a number of third-party codes and these should be referenced appropriately when their functionality is used:

* Geometry optimization or transition state finding:
  * J. Kästner, J.M. Carr, T.W. Keal, W. Thiel, A. Wander and P. Sherwood, “DL-FIND: An Open-Source Geometry Optimizer for Atomistic Simulations,” J. Phys. Chem. A, 2009, 113, p11856.
  * T. P. M. Goumans, C. R. A. Catlow, W. A. Brown, J. Kästner, and P. Sherwood, “An Embedded _Cluster Study of the Formation ofWater on Interstellar Dust Grains,” Phys. Chem. Chem. Phys., 2009, 11, p5431._
* Dispersion corrections:
  * S. Grimme, J. Antony, S. Ehrlich, and H. Krieg, “A consistent and accurate ab initio parametrization of density functional dispersion correction (DFT-D) for the 94 elements H-Pu,” J. Chem. Phys., 2010, 132, p154104.
  * S. Grimme, S. Ehrlich, and L. Goerigk, “Effect of the damping function in dispersion corrected density functional theory,” J. Comput. Chem., 2011, 32, p1456.
* MAGMA routines for GPU-based matrix diagonalization:
  * S. Tomov, J. Dongarra, and M. Baboulin, “Towards dense linear algebra for hybrid GPU accelerated manycore systems,” Par. Comp., 2010, 36, p232.
