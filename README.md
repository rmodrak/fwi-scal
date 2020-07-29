SPECFEM2D/3D Southern California NOISE TOMOGRAPHY examples
==========================================================


Study area
----------

Roughly a 152.95 km by 152.95 km square, with corners

                                34.60407 N, 117.30906 W
    33.23048 N, 118.94971 W



Coordinate systems
------------------

*simple-coordinate-system*

- the solver operates in a Cartesian system defined by
```
        x = (lon-LON0)*(152922.56110827050)/(LON1-LON0)
        y = (lat-LAT0)*(152359.55004705998)/(LAT1-LAT0)
```

- all models currently implemented


*utm-coordinate-system*

- the solver operates in proper UTM coordinates (UTM zone 11)
- so far, only a single model is implemented (3D homogeneous)


Stations and events
-------------------

Station locations are taken from [Groundwater Google Drive](https://drive.google.com/file/d/13H8faW8N4OlIfpxK8yCxqXXcAZ2mNJZo/view?usp=sharing)

Because these are noise tomography examples, event locations in `SOURCE` (2D) and `FORCESOLUTION` (3D) files exactly coincide with station locations.


2D Models
---------

*homogeneous*
- homogeneous
- acoustic


*coarse*
 - 2x2 alternating positive and negative Gaussian variations
 - +10/-10 percent variations
 - acoustic



3D Models
---------

*homogeneous*
- same as 2D homogeneous examle above


*coarse* 
- same pattern of positive and negative Gaussian variations as 2D example 
- 1D depth profile based on Kanamori 1977
- +10/-10 percent variations across all depths
- constant VP/VS = sqrt(3)
- isotropic elastic


*fine*
- 8x8 alternating positive and negative Gaussian variations superimposed on homogeneous model
- +10/-10 percent variations at 0.1 km, decreasing to +0.03/0.03 percent at 1 km
- constant VP/VS = sqrt(3)
- isotropic elastic
