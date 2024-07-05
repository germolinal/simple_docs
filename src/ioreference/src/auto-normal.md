# Normal

 Represents a physical material"
 with common physical properties (e.g.,"
 timber, concrete, brick, glass).  In other words,"
 it cannot change its thermal/optical properties based"
 on its internal state (e.g., it cannot change its specific heat"
 based on temperature, like Gas or Phase Change Materials)."
"
 ## Examples"
"
 #### `.spl`"
"
 ```json"
 {{#include ../../../model/tests/scanner/substance_normal.spl}}"
 ```"
"
 #### `.json`"
"
 ```json"
 {{#include ../../../model/tests/scanner/substance_normal.json}}"
 ```"


 ## Full Specification

```json
Normal {
   name : string,
   thermal_conductivity : number, // optional,
   specific_heat_capacity : number, // optional,
   density : number, // optional,
   front_solar_absorbtance : number, // optional,
   back_solar_absorbtance : number, // optional,
   solar_transmittance : number, // optional,
   front_visible_reflectance : number, // optional,
   back_visible_reflectance : number, // optional,
   visible_transmissivity : number, // optional,
   front_thermal_absorbtance : number, // optional,
   back_thermal_absorbtance : number, // optional,
}
```



#### name

 The name of the Substance. Should be unique for each"
 Substance in the Model object    "




#### thermal_conductivity (*optional*)

 The thermal conductivity of the substance in W/m.K    "




#### specific_heat_capacity (*optional*)

 The specific heat capacity of the substance in J/kg.K"




#### density (*optional*)

 The density of the substance in kg/m3"




#### front_solar_absorbtance (*optional*)

 Solar absorbtance (from 0 to 1) at the front side"
 (Front being the side closer to the first material in a construction)"
"
 Absorbtance is used instead of reflectance (which is used in visible radiation"
 properties) to maintain coherence with EnergyPlus"




#### back_solar_absorbtance (*optional*)

 Solar absorbtance (from 0 to 1) at the front side"
 (Back being the side closer to the last material in a construction)"
"
 Absorbtance is used instead of reflectance (which is used in visible radiation"
 properties) to maintain coherence with EnergyPlus... because in Thermal calculation"
 we mostly care about how much is absorbed; in lighting we care mainly about how much"
 is reflected."




#### solar_transmittance (*optional*)

 The front solar transmittance at normal incidence (from 0 to 1)    "
"
 Please note that, contrary to all other properties, this property"
 does depend on the thickness of the substance. So, in order"
 to build a coherent Glazing, you\'ll need to match this Substance"
 with an appropriate `Material`"
"
 Transmittance is used instead of transmissivity (which is used in visible radiation"
 properties) to maintain coherence with EnergyPlus... because in Thermal calculation"
 we mostly care about how much is absorbed; in lighting we care mainly about how much"
 is reflected."




#### front_visible_reflectance (*optional*)

 Solar absorbtance (from 0 to 1) at the front side"
 (Front being the side closer to the first material in a construction)"
"
 Reflectance is used instead of Absorbtance (which is used in solar radiation"
 properties) to maintain coherence with Radiance... because in Lighting"
 we really care about how much is reflected; in thermal we care mainly about how much"
 is absorbed."




#### back_visible_reflectance (*optional*)

 Solar absorbtance (from 0 to 1) at the front side"
 (Back being the side closer to the last material in a construction)"
"
 Reflectance is used instead of Absorbtance (which is used in solar radiation"
 properties) to maintain coherence with Radiance... because in Lighting"
 we really care about how much is reflected; in thermal we care mainly about how much"
 is absorbed."




#### visible_transmissivity (*optional*)

 The front solar transmittance at normal incidence (from 0 to 1)    "
"
 Please note that, contrary to all other properties, this property"
 does depend on the thickness of the substance. So, in order"
 to build a coherent Glazing, you\'ll need to match this Substance"
 with an appropriate `Material`"
"
 Transmissivity is used instead of Transmittance (which is used in solar radiation"
 properties) to maintain coherence with Radiance"




#### front_thermal_absorbtance (*optional*)

 Front thermal absorbtance (i.e., emissitivy; from 0 to 1)"
 (Front being the side closer to the first material in a construction)"




#### back_thermal_absorbtance (*optional*)

 Back thermal absorbtance (i.e., emissitivy; from 0 to 1)"
 (Back being the side closer to the last material in a construction)"




