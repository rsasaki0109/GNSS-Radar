# GNSS-Radar

Real-time GNSS satellite constellation viewer.

## Demo

https://rsasaki0109.github.io/GNSS-Radar/

## Overview

GNSS-Radar is a web application that shows the current GNSS constellation (GPS, GLONASS, Galileo, BeiDou, QZSS, SBAS) at a specified location. TLE data is fetched live from [CelesTrak](https://celestrak.org/).

Features:
- Satellite ground track on map (Leaflet + ESRI satellite imagery)
- Sky plot (azimuth/elevation) with PRN labels
- Visible satellite count chart (stacked bar)
- DOP (HDOP/PDOP) computation
- Drag-and-drop observer location
- Click chart bar to change time

## URL Parameters

| Parameter | Description | Default | Example |
|-----------|-------------|---------|---------|
| `lat` | Observer latitude (deg) | 35.7 (Tokyo) | `?lat=-37.8` |
| `lon` | Observer longitude (deg) | 139.8 (Tokyo) | `?lon=145` |
| `elemask` | Elevation mask (deg) | 10 | `?elemask=45` |
| `offhr` | Time offset (hours) | 0 | `?offhr=12` |
| `tint` | Time interval (minutes) | 30 | `?tint=5` |
| `ntimes` | Number of time steps | 24 | `?ntimes=48` |

Parameters can be combined: `?lat=35.7&lon=139.8&elemask=15`

## Libraries

- [Leaflet](https://leafletjs.com/) - Map
- [satellite.js](https://github.com/shashwatak/satellite-js) - Satellite orbit propagation (SGP4)
- [Highcharts](https://www.highcharts.com/) - Charts
- TLE data from [CelesTrak](https://celestrak.org/)

## Original

Based on [GNSS-Radar by Taro Suzuki](http://www.taroz.net/GNSS-Radar.html) (2014).
