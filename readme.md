# DeepEM: A Deep Learning Approach for DEM Inversion

The intensity observed through optically-thin SDO/AIA filters (94 Å, 131 Å, 171 Å, 193 Å, 211 Å, 335 Å) can be related to the temperature distribution of the solar corona (the differential emission measure; DEM) as

<center><IMG SRC="./Misc/EqOne.png" width="200"></center>

In this equation, g_i is the DN/s/px value in the <i>i</i>th SDO/AIA channel. This intensity corresponds to the K_i(T) temperature response function, and the DEM, ξ(T), is in units of cm^-5 K^-1. The matrix formulation of this integral equation can be represented in the form, g = <b>K</b>ξ, however, this problem is an ill-posed inverse problem, and any attempt to directly recover ξ leads to significant noise amplication. 

There are numerous methods to tackle mathematical problems of this kind, and there are an increasing number of methods in the literature for recovering the differential emission measure including methods based techniques such as Tikhonov Regularisation (<a href="https://doi.org/10.1051/0004-6361/201117576">Hannah & Kontar 2012</a>), on the concept of sparsity (<a href="https://doi.org/10.1088/0004-637X/807/2/143">Cheung et al 2015</a>). 

In attached notebook, we will demonstrate how a simple 1x1 2D convolutional neural network allows for significant improvement in computational speed for DEM inversion (~10 Million DEM/s on an NVIDIA Quadro P6000) with similar fidelity to the method used for training (Basis Pursuit). Additionally this method, DeepEM, provides solutions with values of emission measure > zero in every temperature bin.

<IMG SRC="./Misc/DeepEMGif2.gif" width="100%">

---

