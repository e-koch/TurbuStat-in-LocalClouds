# TurbuStat-in-LocalClouds

Project advisors: Eric Koch (eric.koch AT cfa.harvard.edu) and Annie Hughes (Annie.Hughes AT irap.omp.eu)

## Project overview ##

We will explore a few different data sets that are all publicly available:

* Perseus from COMPLETE ([Ridge et al. 2006](https://ui.adsabs.harvard.edu/abs/2006AJ....131.2921R/abstract)) [DATA LINK](https://lweb.cfa.harvard.edu/COMPLETE/data_html_pages/FCRAO.html)
* Ophiuchus from COMPLETE ([Ridge et al. 2006](https://ui.adsabs.harvard.edu/abs/2006AJ....131.2921R/abstract)) [DATA LINK](https://lweb.cfa.harvard.edu/COMPLETE/data_html_pages/FCRAO.html)
* Orion from CARMA-NRO ([Kong et al. 2018](https://ui.adsabs.harvard.edu/abs/2018ApJS..236...25K/abstract); [Kong et al. 2021](https://ui.adsabs.harvard.edu/abs/2021RNAAS...5...55K/abstract)) [DATA LINK](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/6Q26PN)

Each of these data sets traces 12CO(1-0) and 13CO(1-0). Because they are highly resolved, we have many options for measuring and comparing the turbulent properties in these clouds:

* Compare entire clouds against each other: Different statistics running on the entire image or data cube.
* Localized variations in turbulence: Splitting each image or data cube into sections, and comparing within and between the clouds.
* Compare different turbulence statistics between 12CO and 13CO: Each tracer is sensitive to a different range in gas volume density. This comparison sheds light on how the ISM structure changes at different volume densities.

The goal of this project is to explore these different possibilities, or beyond if anyone has other ideas they might be interested in exploring. TurbuStat's advantage for these comparisons are its [distance measures](https://turbustat.readthedocs.io/en/latest/tutorials/metrics/running_metrics.html#runmetrics) so that regions can be quantiatively compared, based on turbulence statistics.

Turbulence plays a key role in modern star formation theories, and by comparing between different clouds and regions within clouds, we can test whether turbulent properties vary, how that affects where star formation occurs, and what role stellar feedback has in driving this turbulence.

An overview of each turbulence statistic implemented in TurbuStat is available from the [tutorial page](https://turbustat.readthedocs.io/en/latest/tutorials/index.html).

The two notebooks in this repo show:

1. `data_preprocessing.ipynb` show the preprocessing steps first applied to the publicly available data sets. While these are not strictly necessary, they show how to homogenize some of the data to better compare between the different clouds.

2. `turbustat_overview_localclouds.ipynb` provides some examples of running different turbulence statistics, and how some of the comparisons suggested above can be calculated. These are meant to be a starting point for exploring aspects of the data during the project. They need not be the only types of comparisons you could explore! If you have ideas for other things to explore, please discuss with the supervisors!

## Helpful links ##

[TurbuStat documentations](https://turbustat.readthedocs.io/en/latest/index.html)

[TurbuStat tutorials](https://turbustat.readthedocs.io/en/latest/tutorials/index.html)

NOTE: Each turbulence statistic tutorial includes references to relevant literature. These may not be complete but will provide at least a good starting point to learn more about each technique.

## Some literature on using TurbuStat to compare data sets ##

[Definition of the distance metric - Koch+2017](https://ui.adsabs.harvard.edu/abs/2017MNRAS.471.1506K/abstract)

[Visualizing how feedback affects turbulence statistics - Boyden+2016](https://ui.adsabs.harvard.edu/abs/2016ApJ...833..233B/abstract)

[Comparisons between different spectral line tracers - Boyden+2018](https://ui.adsabs.harvard.edu/abs/2018ApJ...860..157B/abstract)

## Which python packages will you need? ##

* turbustat: `pip install turbustat`

This should install the required packages. To test, open python and run `import turbustat` to check. In case any packages are missing, here is a list of the required packages (see the [turbustat install page](https://turbustat.readthedocs.io/en/latest/install.html) for more details):

* astropy>=2.0
* numpy>=1.7
* matplotlib>=1.2
* scipy>=0.12
* sklearn>=0.13.0
* statsmodels>=0.4.0
* scikit-image>=0.12

These packages can be installed using `pip` or `conda` (if you are using an anaconda environment).

Some of the statistics require additional packages:

* spectral-cube `pip install spectral_cube`
* reproject `pip install reproject`
* radio-beam `pip install radio_beam` (will be installed with spectral-cube)
* astrodendro `pip install astrodendro`
* emcee `pip install emcee`

## Getting the data ##

The different data sets can be downloaded from their public repository (see links above). However, we have gathered them in one place, and applied some preprocessing to some data (not required, but convenient to avoid re-running).

*Contact Eric Koch to get access to the data repository!*
