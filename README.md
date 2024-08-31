# Spectral-decomposition-of-electrical-conductivity

This repository contains Jupyter notebook to calculate spectral decomposition of electrical conductivity from ion velocity data obtained from MD simulations. The theory and corresponding equations can be found in Tu et al. (https://doi.org/10.1063/1.4890741). It contains the following files:

1. test_vel_ion.lammpstrj - example ion velocity data obtained from LAMMPS. Please run your simulations with the following commands:
   ```
   group ion type 3 4
   dump trj_NVT_prod_vel_ion ion custom 10 NVT_prod_vel_ion.lammpstrj element vx vy vz
   dump_modify trj_NVT_prod_vel_ion element O H Cl Na
   dump_modify trj_NVT_prod_vel_ion sort id
   ```

2. self_corr.out - sample output file containing self correlation data
3. cross_corr.out - sample output file containing cross correlation data
4. cond_spec.out - sample output file containing spectral decomposition data
5. diff_const.out - sample output file containing self diffusion constants of ions
6. spec_dec.ipynb - Python code to calculate spectral decomposition of electrical conductivity



