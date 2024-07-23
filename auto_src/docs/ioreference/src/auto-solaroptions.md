# SolarOptions

The options for the solar and lighting calculations

## Examples
##### `.spl`
```json
{{#include ../../../model/tests/scanner/solar_options.spl}}
```
##### `.json`
```json
{{#include ../../../model/tests/scanner/solar_options.json}}
```


 ## Full Specification

```json
SolarOptions {
   n_solar_irradiance_points : int, // optional,
   solar_ambient_divitions : int, // optional,
   solar_sky_discretization : int, // optional,
   optical_data_path : string, // optional,
}
```



#### n_solar_irradiance_points (*optional*)

Number of points utilized to calculate the average incident solar
irradiance over each fenestration or surface in W/m2.

A larger number of points leads to more accurate results but, as usual,
it has an impact on the time of the computation. Specifically,
the time required for creating the model increases linearly with
the number of points. The time required to process each timestep
is not affected.        




#### solar_ambient_divitions (*optional*)

Number of primary rays sent from each of the `n_solar_irradiance_points`
when calculating the average incident solar irradiance over
each surface or fenestration.

A larger number of rays leads to more accurate results but, as usual,
it has an impact on the time of the computation. Specifically,
the time required for creating the model increases linearly with
the number of points. The time required to process each timestep
is not affected.




#### solar_sky_discretization (*optional*)

The sky discretization scheme used for solar irradiance. A value
of 1 leads to 145 sky patches + the ground.

A larger number leads to more accurate results but, as usual,
it has an impact on the time of the computation. Although
the time required for creating the model is not greatly affected,
the time required for processing each timestep can increase considerably.    




#### optical_data_path (*optional*)

A path to the file containing information about solar radiation and other
optical stuff. If the file does not exist, this information will be calculated
and saved in this path. If it does exist, it will be loaded and used directly,
saving time    




