# convert csv to geojson

convert csv to geojson

{% embed url="https://vimeo.com/579431097" %}



## csvkit install

* linux install

```bash
sudo apt install csvkit
```

* mac install

```bash
brew install csvkit
```

## csvcut list columns

```bash
csvcut -n infile.csv
```

* output

```text
1: Name
2: Clerkenwell 101
3: Map
4: Story page
5: Latitude
6: Longitude
7: 101 image
8: Now and then
9: 360 photo
10: People
11: Status
12: Stories
```

## csvjson code

use the --lat option and the name of the column containing the latitude use the --lon option and the name of the column containing the longitude

```bash
csvjson --lat Latitude --lon Longitude infile.csv > geojson.json
```

