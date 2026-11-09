# Egypt rail map

Interactive map of every Egyptian National Railways (ENR) passenger train: 827 trains, 657 stations, 14,934 scheduled stops.

**Live site:** https://salahalshafey.github.io/egypt-rail-map/

- Departure board for every station, with a day picker
- Trip planner for direct trains between any two stations
- Estimated position of every train on the line right now, worked out from the timetable, track distances between stations and the current Cairo time (assumes trains run on time; this is not GPS)
- Full Arabic and English interface (right-to-left layout in Arabic, map labels in either language). Arabic is the default; use the language button, or link straight to a language with `?lang=ar` / `?lang=en`
- Full dataset to download: SQLite, Excel, CSV, GTFS and GeoJSON in [`data/`](data/)

The whole site is one file, `index.html`, with no build step and no server.

## Data sources
- Timetable: checked against the official ENR site (enr.gov.eg/Ar/TrainSchedule.aspx) on 9–10 November 2026; 4,507 stop times were updated. Stops the site did not return keep the values from the ENR timetable database v435 (16 July 2026) as packaged by the Sekka project (github.com/y9090oussefwork/sekka-egypt-train-schedules, MIT). `stop_times.time_source` and `trains.enr_check` say what was verified; `enr_changes` lists every change; trains that could not be checked, or whose times look out of order after the update, are listed in `data_quality`. 13 corrupted day offsets were repaired earlier; see `data_quality`.
- Station locations: OpenStreetMap via egypt-rail-data (ODbL 1.0); GeoNames town centres (CC BY 4.0); positions of stations missing from OpenStreetMap are interpolated from track kilometre posts and marked as estimates.
- Governorate boundaries: egygeo (MIT).

## Licence
The data in `data/` contains OpenStreetMap-derived content and is available under the Open Database License (ODbL) 1.0.
Attribution: © OpenStreetMap contributors, egypt-rail-data contributors, GeoNames, Sekka project.

Unofficial project, not affiliated with Egyptian National Railways. Check times with ENR (enr.gov.eg, hotline 1661) before travelling.
