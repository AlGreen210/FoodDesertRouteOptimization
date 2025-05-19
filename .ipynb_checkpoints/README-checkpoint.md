
# Large Scale Data Analysis of Food Deserts and Route Optimization Development for Food Delivery System. 

## 1.)  Problem Outline:

Globally, lack of access to adequate food is a huge issue. The World Health Organization reports that in 2023, roughly 2.33 billion individuals faced moderate to severe food insecurity.  
With a problem this large even reducing the problem’s scope to just American food insecurity still encompasses 47 million people(USDA).  
A recent cost estimate for ending hunger in the US is 168 billion dollars at a minimum; more realistically it would cost 1.7 trillion dollars spent over 10 years (Hartnett).  
And that estimate dives into the realm of impossibility for our federal government.  
The goal of this project is to address a specific subsection of people who fall under the food insecure umbrella, those living in food deserts, and tackle one of their biggest hurdles: proximity.  
The term food desert denotes geographical areas that are greater than a set number of miles away from a supermarket (1 mile for urban areas and 10 miles for rural areas).  
People who live in these food deserts tend to have poorer total health and financial outcomes when compared to those outside of food deserts.  
From the position of a task force associated with Feeding America, our team aims to start a new mobile farmers market initiative where modified food trucks bring the supermarket to the people instead of shuttling the people to the market.  
But given the constraints of budget discussed earlier and the limitation of time these communities can be served, how can we be sure to maximize the impact?  
Our objective is to use network analysis and route optimization algorithms to carve out a path that considers population and distance to plan a route for the mobile farmers market from the organization headquarters.  

## 2.) Table of Contents:

- Problem Outline
- Table of Contents
- Installation
- Methods/Usage
- Features/ Data Dictionary
- Citations

## 3.) Installation:

Required Libraries to run notebooks:
Import pandas as pd
import numpy as np
import geopandas as gpd
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt
from matplotlib.patches import Patch
from matplotlib.lines import Line2D
from ortools.constraint_solver import routing_enums_pb2
from ortools.constraint_solver import pywrapcp
import networkx as nx
from shapely.geometry import LineString
import os
import math
import matplotlib.cm as cm
from matplotlib.animation import FuncAnimation
import csv
import json
from collections import OrderedDict

## 4.) Methods/Usage:

## 5.) Features/ Data Dictionary:

CensusTract/GEOID- The geographic ID for the Census Tract
State- State tract is found in 
County- The county tract is a part of 
LILATract_1And10- Foundational definition of a food desert
LILATract_1And20- Rural areas that have more severe food access conditions due to supermarket distance
LILATract_Vehicle- Low-income/low-access area where more than or equal to 100 individuals lack transportation means
TractKids- Number of kids in census tract
TractSeniors- Number of seniors in census tract 
TractHUNV- Number of housing units in the population without a vehicle
TractSNAP- Number of households within populations receiving SNAP
SNAP_percent- Percent of the population receiving SNAP food assistance
Kids_percent- Percent of the population under 17
Seniors_percent- Percent of population aged 65 and up
Houshold_noVehicle_percent- Percent of households in the population without a vehicle
LILA_POP_Density- A metric that compares the LILA population over total land area in miles
INTPTLAT- Latitude 
INTPTLON- Longitude
Coordinates- Longitude, Latitude
Geometry- shape of census tract 
Centroid- Plot of center point within census tract. 
ALAND/ALAND_miles- Area of land in meters or miles

## 6.) Extension:

While our project currently only provides an optimized route for a smaller portion within Hidalgo County, the algorithm can be applied to other counties and states with minor modifications to the data (replace, US Census Bureau, and USDA Food Atlas data of interest and follow the same general methods outline.) 
Other related connections could be tracking the rate of nutrition-related health conditions (hypertension, diabetes, obesity, etc.) throughout all Census tracts and searching for specific trends in data.

## 7.) Citations:
[Geopandas and Contextily assistance] ‘https://medium.com/@jl_ruiz/plot-maps-from-the-us-census-bureau-using-geopandas-and-contextily-in-python-df787647ef77’
[Networkx Documentation] ‘https://networkx.org/documentation/stable/auto_examples/algorithms/index.html’
[Scikit Learn Documentation] ‘https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.haversine_distances.html’
Collaborators Github Profiles: 
Omar Rodriguez: https://git.generalassemb.ly/meelol
Marlene Prado: https://git.generalassemb.ly/mprado
Sobomabo Lawson: https://git.generalassemb.ly/soblaw
Andranique Green: https://git.generalassemb.ly/algreen59
