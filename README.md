# urban-environments

This repository contains code related to the paper "Using convolutional networks and satellite imagery to identify patterns in urban environments at a large scale".
* code to acquire and process the data is in the ./dataset-collection folder
* Keras implementations of the convolutional neural networks used for this paper are in ./keras-models
* utilities for loading data, preprocessing etc. are in ./keras-utils
* code to train and validate the models, and to produce the analysis and figures in the paper is in the notebooks in the ./land-use-classification folder.

## Creating the Urban Environments dataset

The process we followed has three steps:
* Obtaining land use survey files from Urban Atlas
* Selecting appropriate samples - as (lat,lon) tuples
* Downloading satellite imagery from Google Maps Static API (API key needed)

We plan to make the actual dataset available after further curation and nsuring that this complies with all applicable data licenses of the dataset used. In the meantime, we describe below the detailed procedure used to construct this dataset. 

#### Obtaining shape files for ground truth labels
First, manually download GIS polygon data for ground truth, available as shapefiles at http://www.eea.europa.eu/data-and-maps/data/urban-atlas.
Unfortunately there is no way to automate this because of the confirmation web forms used on the Urban Atlas website.

The paper uses the shapefiles for 
* Athens
* Barcelona
* Berlin
* Madrid
* Budapest 
* Roma

We have experimented with data for several other cities, however we decided to only include the above six cities in the analysis in the paper. 

#### Selecting appropriate samples
This step is outlined in ./dataset-collection/Urban Atlas - generate sampling locations for training.ipynb
This step can be skipped and just the appropriate 

#### Downloading satellite imagery
This step is outlined in ./dataset-collection/Urban Atlas - extract images.ipynb

