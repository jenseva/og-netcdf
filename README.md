# og-netcdf
Repo for testing Spray glider data in OG NetCDF format.

## Repo includes:

* [Script to generate the NetCDF (Python Notebook)](
https://github.com/jenseva/og-netcdf/blob/main/og-netcdf-spray.ipynb)

* [Sample .nc file that loads into Panoply and ERDDAP well](https://github.com/jenseva/og-netcdf/blob/main/og-netcdf-1.nc)

* [CDL of the sample file](https://github.com/jenseva/og-netcdf/blob/main/og-netcdf-1.cdl)

* [Data from .nc visualized in ERDDAP](https://github.com/jenseva/og-netcdf/blob/main/og-netcdf-erddap-graph.png)

## Test 1 
The first test was to generate a sample .nc file to test the dataset structure in the latest OG-1.0 CDL example template. This test does not attempt to implement all metadata.  

### Goals
* Use Spray data to test making OG-1.0 NetCDF files.  
* Initial tests will be to test the NetCDF format. 
* There are currently questions about how the proposed CDL works with CF aware software like Panoply and in ERDDAP.

### Summary
* Generated a test NetCDF file using the latest OG-1.0 CDL example template. 
* The .nc file did not work as I would have hoped in Panoply or ERDDAP. 
* I've generated a modified CDL that works better in Panoply and ERDDAP. Per CF guidance and the NCEI NetCDF templates it needed Trajectory dimension and I moved Params dimension to variables. 
* Params dimension changes are open for discussion. The OG-1.0 intent of the Params dimension and variable was not clear.
* This repo contains the modified .cdl and sample .nc file 
* It also contains a python notebook that anyone can use to reproduce the .nc file, tweak the format or try on another dataset in the DAC ERDDAP

### References
- [Latest draft CDL (instrument scalar_v2)](
https://github.com/OceanGlidersCommunity/OG-format-user-manual/blob/main/sp041_20191205T1757-instrument-scalar_v2.cdl)
- [Latest draft OG-1.0 Format User Manual](
https://github.com/OceanGlidersCommunity/OG-format-user-manual/blob/main/OG_Format.adoc)  
- [CF 1.8 conventions](https://cfconventions.org/Data/cf-conventions/cf-conventions-1.8/cf-conventions.html#trajectory-data)  
- [NCEI NetCDF 2.0 templates](https://www.ncei.noaa.gov/data/oceans/ncei/formats/netcdf/v2.0/index.html) 

### Notes
* The format user manual and the latest .cdl refeence different CF conventions. I started writing this in CF 1.7 (per the user manual?) but the latest example CDL is CF 1.8. Note to update the user manual.


