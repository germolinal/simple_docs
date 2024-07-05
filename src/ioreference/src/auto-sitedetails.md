# SiteDetails

 Some information about the site in which the building(s) are located"
"
 # Examples"
"
 #### `.spl`"
 ```json"
 {{#include ../../../model/tests/scanner/site_details.spl }}"
 ```"
  #### `.json`"
 ```rs"
 {{#include ../../../model/tests/scanner/site_details.spl }}"
 ```"


 ## Full Specification

```json
SiteDetails {
   altitude : number, // optional,
   terrain : TerrainClass, // optional,
   latitude : number, // optional,
   longitude : number, // optional,
   standard_meridian : number, // optional,
}
```



#### altitude (*optional*)

 The altitude of the site."




#### terrain (*optional*)

 The kind of terrain"




#### latitude (*optional*)

 In degrees. South is negative and North is positive"
"
 This value is irrelevant if a simulation is ran based"
 on an EPW weather file (in which case it is extracted"
 such file). However, it can be useful when producing"
 synthetic weathers or HVAC sizing, or other applications."




#### longitude (*optional*)

 In degrees. West is negative, east is positive."
"
 This value is irrelevant if a simulation is ran based"
 on an EPW weather file (in which case it is extracted"
 such file). However, it can be useful when producing"
 synthetic weathers or HVAC sizing, or other applications."




#### standard_meridian (*optional*)

 In degrees. This is 15*GMT Time Zone"
"
 This value is irrelevant if a simulation is ran based"
 on an EPW weather file (in which case it is extracted"
 such file). However, it can be useful when producing"
 synthetic weathers or HVAC sizing, or other applications."




