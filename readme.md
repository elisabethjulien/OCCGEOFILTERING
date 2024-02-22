#from R package Flexsdm
Velazco, S.J.E., Rose, M.B., de Andrade, A.F.A., Minoli, I. and Franklin, J., 2022. flexsdm: An r package for supporting a comprehensive and flexible species distribution modelling workflow. Methods in Ecology and Evolution, 13(8), pp.1661-1669.


Perform geographical filtering on species occurrences
Description
This function perform geographical filtering of species occurrences based on different approach to define the minimum nearest-neighbor distance between points.

Usage
occfilt_geo(data, x, y, env_layer, method, prj = "+proj=longlat +datum=WGS84")

Arguments

data	
data.frame. Data.frame or tibble object with presences (or presence-absence) records, and coordinates

x	
character. Column name with longitude data

y	
character. Column name with latitude data

env_layer	
SpatRaster. Raster variables that will be used to fit the model

method	used to perform geographical thinning. Pairs of points are filtered based on a geographical distance criteria.The following methods are available:

defined: records are filtered based on a distance value (d) provided in km. Usage method: method = c('defined', d = 300).

prj	
character. Projection string (PROJ4) for occurrences. Not necessary if the projection used is WGS84 ("+proj=longlat +datum=WGS84"). Default "+proj=longlat +datum=WGS84"

