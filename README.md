# rcm-ard-stac-examples

[français](https://github.com/eodms-sgdot/rcm-ard-stac-examples/tree/main?tab=readme-ov-file#aper%C3%A7u)

## Overview
This repository contains the following example workflows for accessing and manipulating analysis-ready data (ARD) products based on RADARSAT Constellation Mission (RCM) imagery from NRCan's Earth Observation Data Management System (EODMS) SpatioTemporal Asset Catalog (STAC) in JupyterLab Python Notebooks:
- [rcm_ard_stac_example.ipynb](https://github.com/eodms-sgdot/rcm-ard-stac-examples/blob/main/examples/rcm_ard_stac_example.ipynb) - instructions on how to access ARD products from the STAC catalog by identifying specific RCM scenes based on a datetime range and spatial bounding box.
- [mchi_decomposition.ipynb](https://github.com/eodms-sgdot/rcm-ard-stac-examples/blob/main/examples/mchi_decomposition.ipynb) - separation of an RCM-ARD image into surface (or single/odd) bounce, volume, and double (or even) bounce  scattering components.
- [coordinate_transformations.ipynb](https://github.com/eodms-sgdot/rcm-ard-stac-examples/blob/main/examples/coordinate_transformations.ipynb) - examples of how to read data directly from the STAC into various coordinate reference systems and reprojecting them to match the projection of other raster arrays already loaded in memory.

### Links
- [Registry of Open Data on AWS - RCM CEOS Analysis Ready Data](https://registry.opendata.aws/rcm-ceos-ard/)
- [rcm-ard collection on EODMS STAC API](https://www.eodms-sgdot.nrcan-rncan.gc.ca/stac/collections/rcm-ard)
- [STAC Browser Overview - RADARSAT Constellation Mission, CEOS-ARD](https://radiantearth.github.io/stac-browser/#/external/www.eodms-sgdot.nrcan-rncan.gc.ca/stac/collections/rcm-ard?.language=en)

## Requirements

### Python
The example notebooks have been tested using Python >= 3.10. To avoid conflicts with package versions it is recommended to create a new virtual environment specific to the repository with `venv` or `conda`.

Using `venv`:
https://docs.python.org/3/library/venv.html

```bash
> python3.10 -m venv .rcmenv
> source .rcmenv/bin/activate
```

Using `conda`:
https://docs.conda.io/projects/conda/en/stable/user-guide/getting-started.html#creating-environments
```bash
> conda create -n rcmenv python=3.10
> conda activate rcmenv
```


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
| matplotlib | Used to visualize RCM-ARD products after reading from STAC | https://pypi.org/project/matplotlib/ |

## Setup

1. In a terminal window, clone the repository into your virtual environment. Installation into your system's base Python environment is not recommended:
	```bash
	> git clone https://github.com/eodms-sgdot/rcm-ard-stac-examples.git
	```

2. Install required Python packages:
	```bash
	> cd rcm-ard-stac-examples
    > pip install -r requirements.txt
	```

3. Open a Jupyterlab window in your default browser with:
	```bash
	> jupyter lab
	```


More information on Project Jupyter and working with computational notebooks in JupyterLab is available at https://jupyterlab.readthedocs.io/en/latest/


## Contact

If you have any questions or require support, please contact the EODMS Support Team at eodms-sgdot@nrcan-rncan.gc.ca.

## License

MIT License

Copyright (c) His Majesty the King in Right of Canada, as 
represented by the Minister of Natural Resources, 2025

Permission is hereby granted, free of charge, to any person obtaining a 
copy of this software and associated documentation files (the "Software"), 
to deal in the Software without restriction, including without limitation 
the rights to use, copy, modify, merge, publish, distribute, sublicense, 
and/or sell copies of the Software, and to permit persons to whom the 
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in 
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING 
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER 
DEALINGS IN THE SOFTWARE.

## Aperçu

Ce dépôt contient les exemples de flux de travail suivants, utilisant le langage Python et les "Jupyter notebooks ", permettant d’accéder et de manipuler les données prêtes à l'analyse (DPA) à partir des images de la mission de la Constellation RADARSAT (MCR), issues du catalogue STAC (Spatio-Temporal Asset Catalog) du système de gestion des données d'observation de la Terre (SGDOT) de RNCan :

- [rcm_ard_stac_example.ipynb](https://github.com/eodms-sgdot/rcm-ard-stac-examples/blob/main/examples/rcm_ard_stac_example.ipynb) - instructions pour accéder aux données MCR-DPA du catalogue STAC  par l’identification de scènes de la MCR selon une sélection  de plage de dates et d’une emprise géométrique minimale *(bounding box)*.
- [mchi_decomposition.ipynb](https://github.com/eodms-sgdot/rcm-ard-stac-examples/blob/main/examples/mchi_decomposition.ipynb) - – décomposition  d’une image en polarimétrie compacte de  de la MCR-DPA entre ses composantes de diffusion de surface (ou bond unique/impairs), volumique et double rebond (ou bond pairs). 
- [coordinate_transformations.ipynb](https://github.com/eodms-sgdot/rcm-ard-stac-examples/blob/main/examples/coordinate_transformations.ipynb) - exemples de lecture de données depuis le catalogue STAC dans divers systèmes de référence de coordonnées, suivis de leur reprojection pour assurer la compatibilité avec d’autres rasters déjà en mémoire. 

### Liens
- [Registre des données ouvertes sur AWS - données de la MCR-CEOS prêtes à l’analyse](https://registry.opendata.aws/rcm-ceos-ard/)
- [Collection de données de la MCR-DPA sur l’IPA SGDOT-STAC](https://www.eodms-sgdot.nrcan-rncan.gc.ca/stac/collections/rcm-ard)
- [Aperçu du Navigateur STAC pour visualiser les données de la Mission de la Constellation RADARSAT en format CEOS-DPA](https://radiantearth.github.io/stac-browser/#/external/www.eodms-sgdot.nrcan-rncan.gc.ca/stac/collections/rcm-ard?.language=fra)

## Exigences

### Python

Les  "Jupyter notebooks" données en exemple ont été testés avec  les versions Python >= 3.10. Pour éviter des conflits avec les versions des paquets, il est recommandé de créer un nouvel environnement virtuel spécifique au dépôt en utilisant `venv` ou `conda`.

En utilisant `venv` :
https://docs.python.org/3/library/venv.html

```bash
> python3.10 -m venv .rcmenv
> source .rcmenv/bin/activate
```

En utilisant `conda` :
https://docs.conda.io/projects/conda/en/stable/user-guide/getting-started.html#creating-environments
```bash
> conda create -n rcmenv python=3.10
> conda activate rcmenv
```

### Paquets Python
| Nom du paquet | Utilisation | URL    |
| -------- | ------- | ------ |
| jupyter  | Utilisé pour créer et exécuter des notebooks Python   | https://pypi.org/project/jupyter/ |
| pystac-client | Utilisé pour connecter au catalogue SGDOT-STAC et y effectuer des recherches     | https://pypi.org/project/pystac-client/ |
| stackstac | Utilisé pour charger des données (ou des sous-ensembles de données) du catalogue STAC dans des tableaux de données matricielles *(raster arrays)*      | https://pypi.org/project/stackstac/ |
| rioxarray    | Utilisé pour lire, transformer, et télécharger les tableaux de données matricielles, et étendre la fonctionnalité de xarray avec rasterio    | https://pypi.org/project/rioxarray/ |
| geopandas | Utilisé pour lire et transformer des données vectorielles. Par exemple,  des fichiers GeoJSON contenant des zones d’intérêt | https://pypi.org/project/geopandas/ |
| shapely | Utilisé pour manipuler et transformer la géométrie des données vectorielles | https://pypi.org/project/shapely/ |
| pyproj | Utilisé pour transformer les systèmes de coordonnées | https://pypi.org/project/pyproj/ |
| numpy | Utilisé pour effectuer des opérations mathématiques sur des tableaux de données matricielles | https://pypi.org/project/numpy/ |
| matplotlib | Utilisé pour visualiser les données  MCR- DPA après leur lecture depuis le  catalogue STAC | https://pypi.org/project/matplotlib/ |

Des informations supplémentaires au sujet  projet Jupyter et de  l’utilisation des notebooks computationnels dans JupyterLab sont disponibles à l’adresse suivante: https://jupyterlab.readthedocs.io/en/latest/

## Installation

1. Dans une fenêtre de terminal, clonez le dépôt dans votre environnement virtuel. L’installation dans l’environnement Python par défaut de votre système n’est pas recommandée :
	```bash
	> git clone https://github.com/eodms-sgdot/rcm-ard-stac-examples.git
	```

2.	Installer les paquets de Python requis :
	```bash
	> cd rcm-ard-stac-examples
    > pip install -r requirements.txt
	```

3. Ouvrez une fenêtre JupyterLab dans votre navigateur par défaut avec : 
	```bash
	> jupyter lab
	```

## Contact

 Pour toute question ou demande de soutien, veuillez communiquer avec l’équipe de soutien du SGDOT à l’adresse suivante:  eodms-sgdot@nrcan-rncan.gc.ca.

