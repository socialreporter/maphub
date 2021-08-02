# weather.com url from coordinates

create a weather.com url for a location with latitude and longitude

[https://weather.com/en-GB/weather/today/l/51.524167,-0.10678610](https://weather.com/en-GB/weather/today/l/51.524167,-0.10678610)

## sed command

example csv file with latitude and longitude

```text
51.524167,-0.10678610
```

sed command to prefix latitude and longitude in csv with weather.com url

```bash
sed -i.bak 's#^#https://weather.com/en-GB/weather/today/l/#' input.csv
```

