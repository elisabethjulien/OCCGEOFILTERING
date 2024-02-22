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

method	
character. Method to perform geographical thinning. Pairs of points are filtered based on a geographical distance criteria.The following methods are available:
  
moran: records are filtered based on the smallest distance that reduces Moran's I to values lower than 0.1. Latlong = TRUE if occurrences are in a geographical projection. Usage method: method = c('moran').

cellsize: records are filtered based on the resolution of the environmental variables which can be aggregated to coarser resolution defined by the factor. Usage method: method = c('cellsize', factor = '2').

defined: records are filtered based on a distance value (d) provided in km. Usage method: method = c('defined', d = 300).

prj	
character. Projection string (PROJ4) for occurrences. Not necessary if the projection used is WGS84 ("+proj=longlat +datum=WGS84"). Default "+proj=longlat +datum=WGS84"


.
