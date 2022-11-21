# og-netcdf
Repo for testing Spray glider data in OG NetCDF format.

## Repo includes:

* [Script to generate the NetCDF (Python Notebook)](
https://github.com/jenseva/og-netcdf/blob/main/og-netcdf-spray-demo-sensor-variables.ipynb)

* [Sample .nc file that loads into Panoply and ERDDAP well](https://github.com/jenseva/og-netcdf/blob/main/nc_out_2022_11_21.nc)

* [CDL of the sample file](https://github.com/jenseva/og-netcdf/blob/main/nc_out_2022_11_21.cdl)

* [Data from .nc visualized in ERDDAP](https://github.com/jenseva/og-netcdf/blob/main/Screen%20Shot%202022-11-21%20at%201.31.23%20PM.png)

## Test 1 
The first test was to generate a sample .nc file to test the dataset structure. This test does not attempt to implement all metadata. It focuses on questions about how the data are loaded into Panoply and ERDDAP. I've made some adjustments to the format to get it to load into Panoply and ERDDAP as expected. Both Panoply and ERDDAP are somewhat CF aware and the format needed some adjustments to be CF compliant.

### Adjustments have been made to:
1) Conform to [CF 1.7 conventions](https://cfconventions.org/Data/cf-conventions/cf-conventions-1.7/cf-conventions.html)
2) Follow [NCEI NetCDF 2.0 templates](https://www.ncei.noaa.gov/data/oceans/ncei/formats/netcdf/v2.0/index.html) where relevant
3) Load into Panoply as GeoTraj
4) Load into ERDDAP as CF trajectory


