# rcm-ard-stac-examples


## Overview
This repository contains the following example workflows for accessing and manipulating RCM-CEOS-ARD data products from the EODMS STAC Catalog in Jupyter Notebook format:
- **rcm_ard_stac_example.ipynb** - instructions on how to access data from the STAC catalog by identifying specific RCM scenes based on a datetime range and spatial bounding box.
- **mchi_decomposition.ipynb** - separation of an RCM-CARD image into surface (or single/odd) bounce, volume, and double (or even) bounce  scattering components.
- **coordinate_transformation.ipynb** - examples of how to read data from the STAC directly into various coordinate reference systems, along with reprojecting loaded data to match other raster arrays.

## Requirements

### Python
The example notebooks have been tested using Python >= 3.10.

### Python Packages
| Package Name    | Use | URL    |
| -------- | ------- | ------ |
| jupyter  | Used to create and run Python notebooks    | https://pypi.org/project/jupyter/ |
| pystac-client | Used to connect to and search through the  EODMS STAC catalog     | https://pypi.org/project/pystac-client/ |
| stackstac | Used to load data (or subsets of data) from the STAC catalog into arrays     | https://pypi.org/project/stackstac/ |
| rioxarray    | Used to read, manipulate, and write raster data arrays, extending xarray's functionality with rasterio    | https://pypi.org/project/rioxarray/ |
| geopandas | Used to read and manipulate vector data, such as GeoJSONs containing areas of interest | https://pypi.org/project/geopandas/ |
| shapely | Used to manipulate geometry objects | https://pypi.org/project/shapely/ |
| pyproj | Used to transform coordinate systems | https://pypi.org/project/pyproj/ |
| numpy | Used to perform mathematical operations on data arrays | https://pypi.org/project/numpy/ |
| matplotlib | Used to visualize RCM-CARD products after reading from STAC | https://pypi.org/project/matplotlib/ |
