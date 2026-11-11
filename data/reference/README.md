# JST historical weather data

`JST.csv` - observations from Johnstown-Cambria County Airport (station
JST), 2025. Downloaded from the Iowa Environmental Mesonet ASOS archive.
13,778 rows covering 364 days.

## Before you use this

- **Do not sum the precipitation column.** `p01i` is a running one-hour
  accumulation repeated on every observation within that hour. Summing
  all rows gives 105.59 in for 2025, against a local normal near 44 in.
  Count one reading per clock hour instead; that gives 39.15 in.
- `M` means missing, `T` means a trace of precipitation (under 0.01 in).
- `mslp` is **sea level** pressure. A BME280 reads station pressure. At
  696 m elevation, station pressure is about 0.920x sea level, so the
  real range here is roughly 909 to 954 hPa, not 987 to 1037.
- Pressure appears only on routine hourly observations, so 8,668 of
  13,778 rows have it. This is normal for ASOS.
- Three readings on 2025-04-14 show 69 to 80 mph sustained wind with a
  direction of 0. Likely a sensor fault.
- 2025-11-02 01:54 appears twice with different readings. The clocks
  went back, so that hour occurred twice.
- 2025-12-31 is absent.

## Derived workbook

A cleaned version with unit conversions and daily and monthly summaries
is on the team shared drive, not in this repository.
