# SAED-Time-evolution
Time evolution of radially averaged diffraction profiles from in-situ selected area electron diffraction (SAED) patterns  
  
This code was used for data representation in our paper below:  
**Electron Beam-Induced Artifacts in SEI Characterization: Evidence from Controlled-Dose Diffraction Studies**  
https://pubs.acs.org/doi/10.1021/acsenergylett.4c03337

# Input data
dm files (.dm3/4) or tiff files (.tif)  

# Input parameters
**1. Rotational Average**  
center: center of the diffraction pattern (in pixels), i.e. the zero beam 000  
  
**2. Baseline based on Asymmetric least squares smoothing (ALS) method**  
lam: $\lambda$ for smoothness of the baseline (generally, $10^2$ $\geq$ $\lambda$ $\geq$ $10^9$).  
  
p: Asymmetric Factor [0-1]. Specify weight of points above the baseline in each iteration.  
The asymmetric factor must be between 0 and 1. For positive peaks it should be close to 0 (generally, 0.001 $\geq$ p $\geq$ 0.1), and close to 1 for negative peaks.  
The smaller the asymmetric factor is, the less effect points above the baseline have on baseline in next iteration.  
  
niter: Specify number of iterations.  
The typical value is 10. In each iteration, it will find a baseline, and determine which points will be considered as points above the baseline for next iteration.  
  
Reference: Eilers PH, Boelens HF. Baseline correction with asymmetric least squares smoothing. Leiden University Medical Centre Report. 2005 Oct 21;1(1):5.
