++++++++++++++ READ ME ++++++++++++++
# GIS_Analysis2_FinalProject

Dateiname: main.ipynb

*Autoren*: 
	Nico Paar - Clemens Wallisch - Maximilian Flor

*Goal*: 
	This project is about a spatial analysis in Graz. 
	The goal is to find the most suitable place in Graz for the erection of a new football stadium. The task description is to conduct and document an original, non-trivial, reproducible GIS.

*Data*:

	Most of the data was extracted from OpenStreetMap. External data is listed below. 

		--------------------------------------------------------------------------------
	District boundaries (Overpass Turbo (n.d.). Overpass API web interface. https://overpass-turbo.eu/ (Accessed December 2, 2025))

	- Overpass Code for district boundaries:
	[out:json][timeout:25];
	area["name"="Graz"]->.g;
	relation(area.g)["boundary"="administrative"]["admin_level"="10"];
	out geom;

	--------------------------------------------------------------------------------


	--------------------------------------------------------------------------------
	- DEM (OpenTopography (n.d.). Copernicus GLO-30 Digital Elevation Model. https://portal.opentopography.org/raster?opentopoID=OTSDEM.032021.4326.3
	(Accessed January 15th, 2025))

	
*Environment used*: 
	python 3.10.9 and python 3.11.0

*Common Errors*:
	If error occurs for any package:
	uninstall packages
	upgrade pip 
	reinstall packages

	If errors occur with pyproj, execute the following line at the first place:
	os.environ["PROJ_LIB"] = pyproj.datadir.get_data_dir()
	

*Disclaimer*
	For certain parts of the code, guidance provided by artificial intelligence was utilized.

*Runtime*:
	between 3-5min, depending on the hardware