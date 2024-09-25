---
aliases: 
  - /planning/hosting/technical/data_request.html
---

# Data request

## Data Format

## Variables

For some models the hydrometeor categories may not map directly onto the specified output.  In these cases hydrometeor habits can be left out (for instance if snow and cloud ice are not distinguished), or additional information can be added, e.g., for models with hail. In such cases, please try to follow [the CF conventions](https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html).

### 3D Output Variables, write instantaneous values at 6hr interval

| CF standard name  | short name  |  units |
|:------------------|------------:|-------:|
| geopotential height | zg | m|
| eastward_wind | ua | m/s |
| northtward_wind | va | m/s |
| upward_air_velocity  | wa | m/s |
| temperature | ta | K | 
| relative_humidity | hur | - | 
| specific_humidity | hus | kg/kg | 
| mass_fraction_of_cloud_liquid_water_in_air | clw | kg/kg | 
| mass_fraction_of_cloud_ice_in_air | cli | kg/kg | 
| mass_fraction_of_rain_in_air | qr | kg/kg | 
| mass_fraction_of_snow_water_in_air | qs | kg/kg | 
| mass_fraction_of_graupel_in_air | qg | kg/kg | 


**3D Output Levels:**

```python
import numpy as np
tr = np.arange(100,900,100)
lt = np.arange(850,1025,25)
ua = np.arange(10,90,20)
levels = sorted({1,5,20,150,250,750}.union(tr,lt,ua))
```

### 2D Output Variables, write at 1hr interval

| CF standard name  | short name  |  units | comment |
|:------------------|------------:|-------:|--------:|
| atmosphere_mass_content_of_cloud_condensed_water| clwvi  | kg m-2| |
| atmosphere_mass_content_of_cloud_ice| clivi  | kg m-2| |
| surface_downward_latent_heat_flux | hfls | W m-2| defined upward in CF Standard |
| surface_downward_sensible_heat_flux | hfss | W m-2| defined upward in CF Standard |
| toa_outgoing_longwave_flux | rlut | W m-2 | |
| toa_outgoing_longwave_flux_clear_sky | rlutcs | W m-2| |
| toa_incoming_longwave_flux | rldt | W m-2 | |
| surface_upwelling_longwave_flux_in_air | rlus | W m-2| |
| surface_upwelling_longwave_flux_in_air_clear_sky | rluscs | W m-2| |
| surface_downwelling_longwave_flux_in_air | rldt | W m-2| |
| surface_downwelling_longwave_flux_in_air_clear_sky | rldscs | W m-2| |
| toa_outgoing_shortwave_flux | rsut | W m-2| |
| toa_outgoing_shortwave_flux_clear_sky | rsutcs | W m-2| |
| toa_incoming_shortwave_flux           | rsdt | W m-2 | | 
| surface_upwelling_shortwave_flux_in_air | rsus | W m-2 | | 
| surface_upwelling_shortwave_flux_in_air_clear_sky | rsuscs | W m-2 | |
| surface_downwelling_shortwave_flux_in_air | rsds | W m-2 | |
| surface_downwelling_shortwave_flux_in_air_clear_sky | rsdscs | W m-2| |
| precipitation_flux | pr | kg m-2 s-1 | |
| atmosphere_mass_content_of_water_vapor | prw | kg m-2 s-1 | |
| surface_air_pressure | ps | Pa | |
| air_pressure_at_mean_sea_level | psl | Pa ||
| specific_humidity | huss | kg kg-1| 2m above ground |
| air_temperature | tas | K | 2m above ground |
| eastward_wind | uas | m s-1 | 10m above ground |
| northward_wind| vas | m s-1 | 10m above ground |
| surface_temperature | ts  | K | |
| surface_downward_eastward_stress | tauu | N m-2 | |
| surface_downward_northward_stress | tauv | N m-2 | | 
|  cloud_area_fraction | clt  | 1 | |
