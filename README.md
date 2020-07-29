SPECFEM2D/3D Southern California NOISE TOMOGRAPHY examples
==========================================================


STUDY AREA
----------

Roughly a 152.95 km by 152.95 km square, with corners

                                34.60407 N, 117.30906 W
    33.23048 N, 118.94971 W



COORDINATE SYSTEMS
------------------

*simple-coordinate-system*

    - the solver operates in a Cartesian system defined by
        x = (lon-LON0)*(152922.56110827050)/(LON1-LON0)
        y = (lat-LAT0)*(152359.55004705998)/(LAT1-LAT0)

    - all models currently implemented


*utm-coordinate-system*

    - the solver operates in proper UTM coordinates (UTM zone 11)
    - so far, only a single model is implemented (3D homogeneous)


STATIONS
--------

    Station locations are taken from 
    https://drive.google.com/file/d/13H8faW8N4OlIfpxK8yCxqXXcAZ2mNJZo/view?usp=sharing

    Because these are noise tomography examples, event locations in
    SOURCE (2D)/FORCESOLUTION (3D) files exactly coincide with station locations.


2D MODELS
---------

*homogeneous*
    - homogeneous
    - isotropic elastic


*checkers_coarse*
    - 2x2 alternating positive and negative Gaussian variations
    - +10/-10 percent variations across all depths
    - constant VP/VS = sqrt(3)



3D MODELS
---------

*homogeneous*
    - same as 2D homogeneous examle above


*checkers_coarse* 
    - +10/-10 percent variations across all depths
    - depth profile based on Kanamori 1977
    - otherwise same as 2D checkers_coarse examle above


*checkers_fine*
    - 8x8 alternating positive and negative Gaussian variations superimposed on homogeneous model
    - +10/-10 percent variations at 0.1 km, decreasing to +0.03/0.03 percent at 1 km
    - constant VP/VS = sqrt(3)
    - isotropic elastic


