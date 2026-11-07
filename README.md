# Egypt rail map

Interactive map of every Egyptian National Railways (ENR) passenger train: 827 trains, 657 stations, 14,934 scheduled stops.

**Live site:** https://YOUR-USERNAME.github.io/egypt-rail-map/

- Departure board for every station, with a day picker
- Trip planner for direct trains between any two stations
- Estimated position of every train on the line right now, worked out from the timetable, track distances between stations and the current Cairo time (assumes trains run on time; this is not GPS)
- Full dataset to download: SQLite, Excel, CSV, GTFS and GeoJSON in [`data/`](data/)

The whole site is one file, `index.html`, with no build step and no server.

## Data sources
- Timetable: ENR timetable database v435 (16 July 2026) as packaged by the Sekka project (github.com/y9090oussefwork/sekka-egypt-train-schedules, MIT). 13 corrupted day offsets were repaired; see `data_quality`.
- Station locations: OpenStreetMap via egypt-rail-data (ODbL 1.0); GeoNames town centres (CC BY 4.0); positions of stations missing from OpenStreetMap are interpolated from track kilometre posts and marked as estimates.
- Governorate boundaries: egygeo (MIT).

## Licence
The data in `data/` contains OpenStreetMap-derived content and is available under the Open Database License (ODbL) 1.0.
Attribution: © OpenStreetMap contributors, egypt-rail-data contributors, GeoNames, Sekka project.

Unofficial project, not affiliated with Egyptian National Railways. Check times with ENR (enr.gov.eg, hotline 1661) before travelling.
