# Streetview url

[https://developers.google.com/maps/documentation/urls/get-started](https://developers.google.com/maps/documentation/urls/get-started)

## csv file with latitude and longitude

create a csv file with latitude and longitude but dont add a column name as we will do that later

```text
51.525213000000001,-0.106725000000000
```

## prepend streetview url

we want to create a streetview url that looks like this

[https://www.google.com/maps/@?api=1&map\_action=pano&viewpoint=51.525213000000001,-0.106725000000000](mailto:https://www.google.com/maps/@?api=1&map_action=pano&viewpoint=51.525213000000001,-0.106725000000000)

by prefixing the latitude and longitude with

```text
https://www.google.com/maps/@?api=1&map_action=pano&viewpoint=
```

prefix latitude and longitude with the google streetview url

```bash
sed -i.bak 's#^#https://www.google.com/maps/@?api=1\&map_action=pano\&viewpoint=#' input.csv
```

### all options

you can also append heading, pitch and fov to the end of the url

[https://www.google.com/maps/@?api=1&map\_action=pano&viewpoint=51.525213000000001,-0.106725000000000&heading=-45&pitch=38&fov=80](mailto:https://www.google.com/maps/@?api=1&map_action=pano&viewpoint=51.525213000000001,-0.106725000000000&heading=-45&pitch=38&fov=80)

```text
&heading=-45&pitch=38&fov=80
```

### heading

the heading in degrees

```text
&heading=-45
```

### pitch

the pitch

```text
&pitch=38
```

### fov

field of view

```text
&fov=80
```

## sed add double quotes around string

add double quotes to the start and end of the text

```bash
sed -i.bak 's/^/"/;s/$/"/' input.csv
```

## add column header to csv file

add the column header to the csv file after you have created the streetview url we add the header after creating the url otherwise it would have the streetview url and double quotes to the string

```text
Streetview
"https://www.google.com/maps/@?api=1map_action=panoviewpoint=51.525213000000001,-0.106725000000000"
```

## csvjoin

join 2 csv files

```bash
csvjoin input-1.csv input-2.csv > output.csv
```

