# convert csv to geojson

where longitude and latitude are the column names in the csv

```bash
ogr2ogr -f geojson output.json input.csv -oo X_POSSIBLE_NAMES=longitude -oo Y_POSSIBLE_NAMES=latitude -oo KEEP_GEOM_COLUMNS=NO
```
