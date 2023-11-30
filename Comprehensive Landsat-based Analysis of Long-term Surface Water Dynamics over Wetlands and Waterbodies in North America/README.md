# Title 
### Comprehensive Landsat-based Analysis of Long-term Surface Water Dynamics over Wetlands and Waterbodies in North America

# Abstract
Wetlands are considered one of the most valuable ecosystems around the world and provide numerous environmental services, including water purification, flood protection, and habitat for a variety of species. Wetlands loss is an increasing trend due to anthropogenic activities and natural processes. As such, spatial knowledge regarding the extent and dynamics of surface water is demanding for wetland conservation and protection. The Landsat program, with five decades of historical earth observation data, has a unique advantage for monitoring wetland surface water changes and dynamics with 30 m spatial resolution. 266 Ramsar wetland sites in North America were monitored for the past 40 years using the open-access Landsat data within the Google Earth Engine cloud computing platform. Landsat Collection 2 Level-2 surface reflectance products were preprocessed and cloud-screened, and a time series of spectral bands and indices were created. The unsupervised Dynamic Surface Water Extent method classified each image into water classes with different confidence levels. An average overall agreement of 92,97% and an average F-score of 96.31% were achieved in this study. Water occurrence maps, in addition to inundation class and change maps, were created for the entire North America, and quantified spatial information was calculated for Ramsar wetland sites.

# Description
This dataset was produced using surface reflectance data from Landsat Collection 2, collected by Landsat platforms -4, -5, -7, -8, and -9. The data provides a detailed view of the Earth's surface with a resolution of 30 meters. It covers a time range from 1982 to the present. The dataset description is listed below.


![DataDescription](https://github.com/BEEILAB/Publications/assets/148573233/dfc8e998-cbd8-4f22-86e3-b00b8f7ab315)


# Web Application

To view data through our Google Earth Engine web application, visit the link below:

https://ma1375hemati.users.earthengine.app/view/cjrs

The grids of the study area, along with the boundary coordinates from Figure 2 of the article, are listed below.


![Boundary](https://github.com/BEEILAB/Publications/assets/148573233/9706ea24-c9ae-4c92-b265-0a161704ac60)


To use the application, enter the ID of the desired section and click on the "Run" button (See the following  figure).


![Usage](https://github.com/BEEILAB/Publications/assets/148573233/6703e26a-0561-4000-a798-f19df74adee5)



Please note that a lower resolution of the product is shown in the app due to memory limitations.


# Exporting Data
To export data, a Google Earth Engine account is required. If you have not registered, you can register using the the following link:

https://earthengine.google.com/new_signup/ 

Then, To export data, use a boundary box of your desired area or the drawing tools to create a geometry.

### Using Boundary Coordinates

Using the "ExportBoundary" function, input your desired "startyear" and "endyear" in addition to coordinates for the boundary box of the area; for example:
	

```
var WO = require('users/ma1375hemati/CJRS_App:WO_CJRS');
// Using a boundary box
// Inputs: Start year, end year, west, south, east, north
WO.ExportBoundary(1982,2023,-105, 51,-104,52);
```


![GuideGee](https://github.com/BEEILAB/Publications/assets/148573233/3e1bf734-43ef-4e1a-bd64-f4553bfcc3d6)



### Using a Geometry
At first, create your desired geometry using the drawing tools, or import your geometry. After that, using the "ExportGeometry" function, input your desired "startyear", "endyear" and geometry. For example:

```
var WO = require('users/ma1375hemati/CJRS_App:WO_CJRS');
// Using a boundary geometry
// Inputs: Start year, end year, geometry
WO.ExportGeometry(1982,2023,geometry);
```

# Citation

```plaintext
@article{hemati2023comprehensive,
  title={Comprehensive Landsat-based Analysis of Long-term Surface Water Dynamics over Wetlands and Waterbodies in North America},
  author={Hemati, Mohammadali and Mahdianpari, Masoud and Shiri, Hodjat and Mohammadimanesh, Fariba},
  journal={Canadian Journal of Remote Sensing},
  year={2023},
  note={In Press}
}
