# kml to csv

where longitude and latitude are the column names in the csv works for converting csv files to kml for maphub

```bash
ogr2ogr -f LIBKML output.kml input.csv -oo X_POSSIBLE_NAMES=longitude -oo Y_POSSIBLE_NAMES=latitude -oo KEEP_GEOM_COLUMNS=NO
```

