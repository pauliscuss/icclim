
Intro
======

ICCLIM (Indice Calculation CLIMate) is a Python library for computing a number of climate indices.

Currently, the 49 climate indices as defined by `European Climate Assessment & Dataset <http://www.ecad.eu/>`_ based on air temperature and precipitation variables are included:

	- 11 cold indices (GD4, CFD, FD, HD17, ID, CSDI, TG10p, TN10p, TX10p, TXn, TNn)
	- 1 drought indice (CDD)
	- 9 heat indices (SU, TR, WSDI, TG90p, TN90p, TX90p, TXx, TNx, CSU)
	- 14 rain indices (PRCPTOT, RR1, SDII, CWD, R10mm, R20mm, RX1day, RX5day, R75p, R75pTOT, R95p, R95pTOT, R99p, R99pTOT)
	- 4 snow indices (SD, SD1, SD5cm, SD50cm)
	- 6 temperature indices (TG, TN, TX, DTR, ETR, vDTR)
	- 4 compound indices (CD, CW, WD, WW)
	
Detailed description of each indice is available at http://eca.knmi.nl/documents/atbd.pdf.

Initialy ICCLIM was designed for online computing of climate indices through the `climate4impact portal <http://climate4impact.eu>`_. 
In spite of existence of other packages able to compute climate indices (`CDO <https://code.zmaw.de/projects/cdo>`_, `R package <http://etccdi.pacificclimate.org/software.shtml>`_ ),
it was decided to develop a new software in Python.
Python language was first of all choosen to interface with `PyWPS <http://pywps.wald.intevation.org/>`_: Python implementation of Web Proccessing Service
(WPS) Standard.
Another reason was to interface eventially with the `OpenClimateGIS <https://earthsystemcog.org/projects/openclimategis/>`_.

The ICCLIM developer repository can be found here: `<https://github.com/cerfacs-globc/icclim>`_

Notes about ICCLIM
~~~~~~~~~~~~~~~~~~~~

1. Input dataserts must be compliant to the `CF convention <http://cf-pcmdi.llnl.gov/documents/cf-conventions/>`_.
2. Currently, *ICCLIM* doesn't support spatial subsetting, i.e. it processes whole spatial area.
3. *ICCLIM* works with unsecured OPeNDAP datasets as well.


.. _climate_indices_label:

What is a climate indice
~~~~~~~~~~~~~~~~~~~~~~~~~~
A climate index is a calculated value that can be used to describe the state and the changes in the climate system.

The climate at a defined place is the average state of the atmosphere over a longer period of, for example, months or years. Changes on climate are much slower than on the weather, that can change strongly day by day.

Climate indices allow a statistical study of variations of the dependent climatological aspects, such as analysis and comparison of time series, means, extremes and trends.

.. note:: A good introduction for climate indices is on the website of the `Integrated Climate Data Center (ICDC) <http://icdc.zmaw.de/climate_indices.html?&L=1>`_ of the University of Hamburg.

.. seealso::

    - `Climate Variability and Predictability (CLIVAR) <http://www.clivar.org/panels-and-working-groups/etccdi/indices-data/indices-data>`_
    - `Expert Team on Climate Change Detection and Indices (ETCCDI) <http://etccdi.pacificclimate.org/>`_ 
    - `European Climate Assessment & Dataset (ECA&D) <http://eca.knmi.nl/indicesextremes/index.php>`_
    
    
    - `ATBD ECA&D indices <http://eca.knmi.nl/documents/atbd.pdf>`_
    - `Article about percentile-based indices <http://etccdi.pacificclimate.org/docs/Zhangetal05JumpPaper.pdf>`_
    - `Sample quantiles in statistical packages <http://amherst.edu/media/view/129116/original/Sample+Quantiles.pdf>`_
