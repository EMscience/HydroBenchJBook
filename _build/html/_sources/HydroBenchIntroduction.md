# HydroBench - Introduction
[![HydroBench Github Repo](/images/GitHubIcon.png)](https://github.com/EMscience/HydroBench)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/EMscience/HydroBench/HEAD)
[![DOI](https://zenodo.org/badge/375593287.svg)](https://zenodo.org/badge/latestdoi/375593287)

## Hydrological Model Benchmarking and Diagnostics

Hydrological model performances are commonly evaluated based on different statistical metrics e.g., the Nash Sutcliffe 
coefficient ([NSE](https://en.wikipedia.org/wiki/Nash%E2%80%93Sutcliffe_model_efficiency_coefficient)). However, these metrics 
do not reveal neither the hydrological consistency of the model nor the model's functional performances, such as how different 
flux and store variables interact within the model. As such, they are poor in model diagnostics and fail to indicate whether 
the model is right for the right reason. In contrast, hydrological process signatures and information theoretic metrics are 
capable of revealing the hydrological consistency of the model prediction and model internal functions respectively. In this 
notebook, we demonstrate the use of interactive and reproducible comprehensive model benchmarking and diagnostic using:

1) a set of statistical predictive performance metrics: Nash Sutcliffe coefficient, Kling and Gupta coefficient, percent bias and pearson correlation coefficient

2) a set of hydrological process based signatures: flow duration curve, recession curve, time-linked flow duration curve, and runoff coefficient, and

3) information theoretic based metrics, particularly [Transfer Entropy (TE)](https://en.wikipedia.org/wiki/Transfer_entropy) and [Mutual Information(MI)](https://en.wikipedia.org/wiki/Mutual_information). 

The application of these metrics is demonstrated on the the National Hydrologic Model product using the PRMS model ([NHM-PRMs](https://www.sciencebase.gov/catalog/item/58af4f93e4b01ccd54f9f3da)). 
NHM-PRMS has two model products covering the CONUS - the calibrated and uncalibrated model products. 
Out of the CONUS wide NHM-PRMS products, this notebook focused on the NHM-PRMS product at the 
[Cedar River, WA](https://waterdata.usgs.gov/nwis/nwismap/?site_no=12115000&agency_cd=USGS). 

