# Pankaj notes
* I have manully created the directory "scratch" within each test directory 
* Added package MAT to read and write MATLAB data
* Added SEAM Phase 1 model for the joint inversion project 
* notice float64 to float32 conversion after reading the velocity model
* I am working with Julia_1.5   
:wq





# COFII framework examples 

This series of jupyter notebooks demonstrates features of the `Chevron Optimization Framework for Imaging and Inversion`.

* The notebooks are intended to be run in order. 
* Downstream notebooks may depend on artifacts created in previous notebooks. For example the Marmousi dataset is downloaded and processed in the series `20_marmousi_model_setup`, and used in subsequent notebooks.   :wq
* Some notebooks may require reasonable HPC resources to run. For example the FWI and RTM examples can run for more than one hour, depending on what hardware you execute them on. 


## Brief description of notebook series
* `00_add_packages` adds and precompiles all packages used in these demos.
* `10_jets_basics` introduction to `Jets` and `DistributedJets`.
* `20_marmousi_model_setup` download the Marmousi model.
  * The Marmousi 2 model is provided by the Allied Geophysical Laboratory of the University of Houston, license and more information at the SEG wiki entry 
  [AGL Elastic Marmousi](https://wiki.seg.org/wiki/AGL_Elastic_Marmousi).
  * If you run these notebooks you will have a copy of the license to review in the directory `20_marmousi_model_setup`.
* `30_forward_modeling` static and dynamic scheduled modeling.
* `40_single_trace_sensitivity` generation of FWI sensitivity kernel.
* `50_fwi` brute force Marmousi time domain FWI using the `LBFGS` algorithm from `Optim.jl`, includes upsampling and downsampling models, data analysis, illumination compensation, very simple box constraints, and nonlinear optimization using `Optim.jl`.  
* `60_rtm` brute force RTM of the Marmous FWI results, including data processing like applying a temporal mute, and image processing like a Laplacian filter to remove backscattered noise. Both static and dynamic scheduled examples are provided. 
