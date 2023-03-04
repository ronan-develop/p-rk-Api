# P@rkPMR

This project is
under [licence GNU Lesser General Public License (LGPL), version 3](./licence.md)

You need to install `Ogr2Ogr` to convert and
manipulate GeoJson.On Windows, QGIS is needed for ogr2ogr in CLI.
`PostGIS` is a spatial database extender for `PostgreSQL` object-relational database.
It adds support for geographic objects allowing location queries to be run in SQL.
Feature List [here](https://www.postgis.net/features/)

## Tools

| Name    |                          Link                           |                  Utility                  |
|---------|:-------------------------------------------------------:|:-----------------------------------------:|
| Docker  | [here](https://www.docker.com/products/docker-desktop/) |               Build Images                |
| ogr2ogr |     [here](https://gdal.org/programs/ogr2ogr.html)      |              Convert GeoJson              |
| QGIS    | [here](https://qgis.org/en/site/forusers/download.html) |          For ogr2ogr on Windows           |
| PostGIS |       [Docs & Download](https://www.postgis.net/)       | Spatial database extender for PostgreSQL. |

command to inject `geoJson` data :
```bash
ogr2ogr -f "PostgreSQL" PG:"host=localhost user=postgres password=ronanpass dbname=postgres" places-de-stationnement-pmr.geojson -nln park
```
this will create database `park` tables and rows.