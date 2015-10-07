# 

Modification of Growth with CAMB (MGCAMB)


By [A. Hojjati](http://www.phas.ubc.ca/~ahojjati/index.html "Home.html"), [G.-B. Zhao](http://icosmology.info/), [L. Pogosian](http://www.sfu.ca/%7Elevon/) and [A. Silvestri](http://space.mit.edu/home/asilvest/Homepage.html)

| 

[Our paper](http://arxiv.org/abs/1106.4543)

[Description](#description)

[Download and Installation](#download)

[Several examples](Models.html)

[](#download)[Implementation in CosmoMC](#Cosmomc)

[Version History](#Version)

[Referring to this code](#reference)

 |

## <a name="description"></a>Description

[CAMB](http://camb.info/) is a public fortran 90 code written by Antony Lewis and Anthony Challinor for evaluating cosmological observables. MGCAMB is a modified version of CAMB in which the linearized Einstein equations of General Relativity (GR) are modified. MGCAMB can also be used in [CosmoMC](http://cosmologist.info/cosmomc/) to fit different modified-gravity (MG) models to data.

This parametrization is discussed in detail in the [paper](http://arxiv.org/abs/1106.4543). The initial conditions for the evolution of linear perturbations are not modified in the current version of MGCAMB. A discussion of initial conditions can be found in the [paper](http://arxiv.org/abs/1106.4543). Some of the widely used functional forms for such parametrization are reviewed and implemented in the code, while others can also be easily implemented. Several examples can be found [here](http://aliojjati.github.io/MGCAMB/Models.html).

## <a name="download"></a>Download and Installation

There are two ways to get MGCAMB. The easy way is to replace some of the files in CAMB with the modified versions supplied [here](http://aliojjati.github.io/MGCAMB/source_files/MGCAMB-files.html) and re-compile the code. You should get the modified version of the following files:
`
params.ini
inidriver.F90
equations.f90

`In this case, attention must be paid for the compatibility of the version used.

The other way is to manually modify your existing code. For instructions, click [here](http://aliojjati.github.io/MGCAMB/MGCAMB-instructions.html).

## <a name="Cosmomc"></a>Implementation in CosmoMC

Using MGCAMB with Cosmomc requires passing the new MG variables to the CosmoMC routines. Again, you can download the modified files directly from [here](http://aliojjati.github.io/MGCAMB/source_files/MGcosmomc-files.html). You should get the following files :

`params.ini
params_CMB.paramnames
source/driver.F90
source/settings.f90
source/CMB_Cls_simple.f90
source/cmbtypes.f90
source/params_CMB.f90
`

To manually modify your existing code, follow the steps [here](http://aliojjati.github.io/MGCAMB/MGcosmomc-instructions.html).

## <a name="Version"></a>Version History

**February, 2014:** **Major upgrade** to CosmoMC, March 2013 version. Planck data can now be used.

**December, 2013:** Bug fixes thanks to Bin Hu and Jasson Dossett.

**February, 2012:** MGCAMB, January-12 version.

**January, 2012:** MGCAMB, October-11 version.**July, 2011:** MGCAMB, July-11 version.

This version (V.2) of MGCAMB is written based on CAMB (instead of [CAMBsources](http://camb.info/sources/)) which makes it easier to use with Cosmomc. It also generalizes the previous parametrization making it applicable to the entire range of redshifts and includes different components of the energy-momentum tensor. It also includes other modified-gravity parametrizations introduced in the literature.

The [previous](http://icosmology.info/website/MGCAMB.html) version of MGCAMB written by G.B. Zhao, L. Pogosian, A. Silvestri and J. Zylberberg was based on [CAMBsources](http://camb.info/sources/). That version modified GR equations for z>30, i.e. at late times when the contribution of radiation is negligible.

## <a name="reference"></a>Reference to this code

If you use MGCAMB, please cite the original [CAMB](http://camb.info/) [paper](http://arxiv.org/abs/astro-ph/9911177) and our papers:

<span class="style_8">**-- Testing gravity with CAMB and CosmoMC**
</span>

<span class="style_8">AH,</span> <span class="style_10">Levon Pogosian and Gong-Bo Zhao
</span>

[arXiv: 1106.4543](http://arxiv.org/abs/1106.4543 "http://arxiv.org/abs/1106.4543")<span class="style_8">
</span>

<span class="style_8">**--Searching for modified growth patterns with tomographic surveys**
</span>

<span class="style_10">Gong-Bo Zhao, Levon Pogosian, Alessandra Silvestri and Joel Zylberberg</span>[
](http://arxiv.org/abs/0809.3791 "http://arxiv.org/abs/0809.3791")

[arXiv: 0809.3791
](http://arxiv.org/abs/0809.3791 "http://arxiv.org/abs/0809.3791")

[
](http://arxiv.org/abs/0809.3791 "http://arxiv.org/abs/0809.3791")

_**If you have any questions or comments, or want to be notified of MGCAMB updates, please send an email to** a_hojjati@sfu.ca_

[![Locations of visitors to this page](http://www2.clustrmaps.com/stats/maps-no_clusters/www.sfu.ca-~aha25-thumb.jpg)](http://www2.clustrmaps.com/user/69bd8bc6) 
Last updated on February, 4, 2014.
