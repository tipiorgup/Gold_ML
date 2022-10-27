# DFTB-Neural-Net

## Description
Correction of DFTB potential energy surfaces into PBE using the $\Delta$-learning neural network. 

## Installation
Here you will find the steps to install **DFTB+** code and python dependencies necessary to run the code. 

1. git clone -b machine-learning https://github.com/tomaskubar/dftbplus.git 
2. cd dftbplus
3. module load gnu8/8.3.0
4. module load openblas/0.3.7
5. module load cmake
6. mkdir _build 
7. FC=gfortran CC=gcc cmake -DCMAKE_INSTALL_PREFIX=$HOME/opt/dftb+ -B _build .
8. cmake --build _build -- -j 
9. cmake --install _build

```diff 
+ Check if the `dftb+` executable exist in the dftbplus/_build/prog/dftb+/ folder. If so, then everything is okay. 
```

## Content/:
 In the "Normal" folder you will find the training with Au79 using no affiny energies to normalize the data, ie. we use the input as it comes from deMon2k and DFTB.
 This is an attemp to eliminate the bias caused by Au79 reference dataset.
 
 I am trying different sets of hyperparameters but deleating this normalization makes a greater error on the TestSet.
 This week I will try data normalization (mean and standard deviation).
 
 We can try the current model and check the new slopes.


Please provide samples nanoclusters of different sizes in the folder to test. 
Thank You!
