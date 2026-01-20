# GIS_Analysis2_FinalProject
(Aktuell privat, wird später geändert)
Nico Paar - Clemens Wallisch - Maximilian Flor

To do Liste: 
1. Analyseverfahren mit Ausschlusskriterien (Als Layer)
Gewässer (OSM = Water) + Buffer 10m (Shape drinnen, reprojected & buffered) -gemacht
Erholungsflächen (OSM Leisure = Park) (drinnen, kein Buffer) - gemacht
Verkehrsflächen (Buffer notwendig) - gemacht
Schule, Kindergarten, Krankenhaus, Friedhof (Buffer 250m, reprojected, drinnen) -gemacht
Gebäude (Punkte und Linie rausnehmen und nur Polygone verwenden!) -gemacht
Hanglage (max. 5% Steigung) -gemacht

2. merge und dissolve aller flächen und danach von Graz fläche abzeihen

3. Flächen suchen mit mindestens 15 Hektar (150000 m²) und filtern 

4. Scores für Gewichtung (mit Routing evtl. von Autobahnausfahrten aus mit nearest_node)
-->network nx graph für graz downloaden
Abstand zu Wohngebieten
ÖV-Anbindung
Auto Erreichbarkeit (Routing)
Zentrale Lage 
evt. Zentrale Lage (Filter nach Bevölkerung)
Abstand Hospitals Kindergarten Friedhof Kirchen

5. Endanalyse und Visualisierung


All packages have to be installed (pip install...)

All Features in Projection UTM 33N - EPSG: 32633

--------------------------------------------------------------------------------
District boundaries (Overpass Turbo (n.d.). Overpass API web interface. https://overpass-turbo.eu/ (Accessed December 2, 2025))

- Overpass Code for district boundaries:
  [out:json][timeout:25];
  area["name"="Graz"]->.g;
  relation(area.g)["boundary"="administrative"]["admin_level"="10"];
  out geom;

--------------------------------------------------------------------------------
Population statistic (Stadt Graz (2025). Zahlen + Fakten: Bevölkerung, Bezirke, Wirtschaft, Geografie.                                                             https://www.graz.at/cms/beitrag/10034466/7772565/Zahlen_Fakten_Bevoelkerung_Bezirke_Wirtschaft.html (Accessed December 2, 2025))


Districts are two seperate datasets in the data file
download from the link and insert it to the data file

--------------------------------------------------------------------------------
- DEM (OpenTopography (n.d.). Copernicus GLO-30 Digital Elevation Model. https://portal.opentopography.org/raster?opentopoID=OTSDEM.032021.4326.3
  (Accessed January 15th, 2025))


  If error occurs for any package:
  uninstall packages
  upgrade pip 
  reinstall packages