## webapp_phase5

### NYU easy Residence

keywords: Community Districts, Neighbourhoods, map

#### Description of the datasets and function design

| name | link | datatype | data columns used | data amount |
| ---- |:----:| --------:| ----------------- |:-----------:|
|Neighborhood Names GIS |	[link](https://catalog.data.gov/dataset/neighborhood-names-gis) | JSON	| id, name, borough, lat,lng |	300 rows |
|NY Districts geoshapes |	[link](http://services5.arcgis.com/GfwWNkhOj9bNBqoJ/arcgis/rest/services/nycd/FeatureServer/0/query?where=1=1&outFields=*&outSR=4326&f=geojson) |	GeoJson | BoroCD, geometry	| 71 rows
| Crimes in NY |[link](https://data.cityofnewyork.us/api/views/wuv9-uv8d/rows.json?accessType=DOWNLOAD)| JSON |lat, lng, districtId | several
| NY Farmers Markets |[link](https://data.ny.gov/resource/7jkw-gj56.json)| JSON|lat,lng| less than 100
| NY Subway Entrance |[link](https://data.ny.gov/resource/hvwh-qtfg.json)|JSON|entrance_lat, entrance_lng| 1000
 

My project can be used to see information from NY neighbourhoods and also community districts geo data, specifically users can graph the borders of the desired districts and boroughs.

#### Map View:

1. [Y]  Maps:
- Basic Map with specific location ( Map is centered in NYU ).
- SVG map that can be hovered to reveal information about districts.
2. [Y] First map can be covered by the borders of districts, markers of subway entrances and districts centroids, along with a criminality heatmap.

#### Data Visualization:

1. [Y] I use a radar chart to show the strenghts and compare districts, based on differente parameters.
2. [Y] The user can hover the points of the chart to know the exact number.

#### Interaction Form:

1. [Y] 

- Tables with raw data that can be exported as CSV
- Information of specified districts in second map
2. [Y] 
- The user can select from several tables and export them as CSV.
- Rank based on attributes, the zscore of the district is recalculated based on the filters choosen.
3. [Y] 
- The user can choose from 5 different parameters the ones that are used to rank the districts in the table.
- The user can select a unique district to know more about it by hovering it in the map
4. [Y]
- The user can filter the borders, crimes and markers that are drawn in the google map with several filters, the markesr have titles.
5. [Y] 
- First map, when a district from the selected boroughs is hovered the nearest Subway entrance to the district centroid is shown in the map, also the radar chart is updated based on the selected/hovered district
- Second map, when a district is hovered it highlights in yellow.

Tested on Firefox and Chrome