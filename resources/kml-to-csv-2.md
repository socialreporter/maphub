# kml to csv

GEOMETRY: By default, the geometry of a feature written to a .csv file is discarded.

It is possible to export the geometry in its WKT representation by specifying GEOMETRY=AS~WKT~. It is also possible to export point geometries into their X,Y,Z components \(different columns in the csv file\) by specifying GEOMETRY=AS~XYZ~, GEOMETRY=AS~XY~ or GEOMETRY=AS~YX~. The geometry column\(s\) will be prepended to the columns with the attributes values.

this will create x and y colums in the csv file, where x is longitude and y is latitude

```bash
ogr2ogr -f CSV output.csv input.kml -lco GEOMETRY=AS_XY
```

