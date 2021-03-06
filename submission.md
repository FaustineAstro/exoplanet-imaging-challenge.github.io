---
layout: page
title: Submission instructions
---

This challenge will consist of two consecutive stages (with two sub-challenges running in parallel), each one with its own type of submission and metrics. 

**Stage 1**: The expected output from an algorithm, i.e. the submission from a given participant, consists of a list of detection maps (nine for the first sub-challenge and ten for the second) and a single detection threshold per sub-challenge (the accepted threshold at which a detection is claimed). Optionally, the [FHWM](https://en.wikipedia.org/wiki/Full_width_at_half_maximum) values used for each dataset can be submitted. The FWHM values are related to the expected size of detected blobs (resolution element) on the detection maps. Every file must be in FITS format, please check out the documentation of the [Astropy Python library](http://docs.astropy.org/en/stable/io/fits/) if you want to know more about saving data in FITS format. Optionally, the [VIP Python library]((https://github.com/vortex-exoplanet/VIP)) contains a wrapper (``vip_hci.fits.write_fits()``) of Astropy for saving Python numpy arrays as FITS files.

For example, for generating a submission file to the second sub-challenge (ADI+mSDI) you must compile the following files in *zip* format: 

* ``detection_threshold.fits`` (scalar value),
* ``gpi_detmap_1.fits`` (2d array),
* ``gpi_detmap_2.fits`` (2d array), 
* ``gpi_detmap_3.fits`` (2d array), 
* ``gpi_detmap_4.fits`` (2d array), 
* ``gpi_detmap_5.fits`` (2d array), 
* ``sphere_ifs_detmap_1.fits`` (2d array), 
* ``sphere_ifs_detmap_2.fits`` (2d array), 
* ``sphere_ifs_detmap_3.fits`` (2d array), 
* ``sphere_ifs_detmap_4.fits`` (2d array), 
* ``sphere_ifs_detmap_5.fits`` (2d array). 

Optionally, you can include:

* ``gpi_fwhm_1.fits`` (scalar value), 
* ``gpi_fwhm_2.fits`` (scalar value),
* ``gpi_fwhm_3.fits`` (scalar value),
* ``gpi_fwhm_4.fits`` (scalar value),
* ``gpi_fwhm_5.fits`` (scalar value), 
* ``sphere_ifs_fwhm_1.fits`` (scalar value), 
* ``sphere_ifs_fwhm_2.fits`` (scalar value), 
* ``sphere_ifs_fwhm_3.fits`` (scalar value), 
* ``sphere_ifs_fwhm_4.fits`` (scalar value), 
* ``sphere_ifs_fwhm_5.fits`` (scalar value). 

{: .box-note}
**Note:** Each submission must correspond to the results of applying **a single algorithm to all the datasets**. If your algorithm works for both 3D and 4D datasets then you need to make two submissions (to have your score on each scoreboard). Please keep in mind that a partial submission for a given sub-challenge is possible, but that will penalize the metrics computations and your score. 

**Stage 2**: This expensive procedure will be performed locally, therefore the source code of the algorithm (implemented on an open source language such as Python or R), an executable file or a Docker image will be required from the participants. Additionally, each participant must submit a single detection threshold (per sub-challenge) to be used during the thresholding and blob counting procedures.

{: .box-warning}
**Important:** this stage of the data challenge will only be conducted if enough participants demonstrate their interest in submitting/sharing their code. 



