# sos-rotation-averaging
Certifiably globally optimal unit quaternion rotation averaging via Sparse Bounded-degree sum of squares optimization.

<img src="https://raw.githubusercontent.com/utiasSTARS/sos-rotation-averaging/master/rotation_averaging.png" width="500px"/>

## Installation and Dependencies 

All code and experiments were developed in Matlab R2017b.

We use the [Sparse-BSOS](https://github.com/tweisser/Sparse_BSOS) Matlab package, which ships with its own modified version of SDPT3 (see the linked repository for setup details).

We use the [CVX](http://cvxr.com/cvx/) modelling language, which is free for academic usage. The default SDPT3 solver that ships with CVX was used.

Our plotting script makes use of the [`subaxis`](https://www.mathworks.com/matlabcentral/fileexchange/3696-subaxis-subplot) function to create subplots. 

## Usage 
All code is found in the folder `matlab/`. Be sure to add this folder, its subfolders, and all dependencies to your Matlab path.

### Plotting Script
The code for error and cost function plots appearing in our [paper](http://arxiv.org/abs/1904.01645) (see below) can be run with the script `matlab/plot_error_figures.m`. This script uses the `.mat` files containing experimental results in `data/`. The data files are accessed with relative paths, so be sure to run the script from within the `matlab/` folder.

### Rotation Averaging Example Script
The script `matlab/results_rotation_averaging_sbsos_odom.m` shows a sample usage of our main contribution, the function `matlab/rotation_averaging_sbsos.m` on simulated noisy data. The script `matlab/results_rotation_averaging_sbsos_dual.m` compares our approach with an SDP-relaxation. 

## Citation
If you use any of this code in your work, please cite the [relevant publication](http://arxiv.org/abs/1904.01645): 

```bibtex
@article{giamou2019sparse,
  title={Sparse Bounded Degree Sum of Squares Optimization for Certifiably Globally Optimal Rotation Averaging},
  author={Giamou, Matthew and Maric, Filip and Peretroukhin, Valentin and Kelly, Jonathan},
  journal={arXiv preprint arXiv:1904.01645},
  year={2019}
}

```
