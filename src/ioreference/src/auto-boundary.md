# Boundary

 Represents the boundary of a `Surface`"
"
 By default (i.e., if no boundary is assigned to a `Surface`),"
 the boundary will be assumed to be outside."
"
 > **Note**: This object cannot be declared by itself in a `SIMPLE` model. It is always"
 embedded on a `Surface`"
"
 ## Examples"
"
 #### A `Space` boundary (in `.json`)"
 ```json"
 {{#include ../../../model/tests/scanner/boundary_space.json}}"
 ```"
 #### A `Ground` boundary (in `.json`)"
 ```json"
 {{#include ../../../model/tests/scanner/boundary_ground.json}}"
 ```"


 ## Supported Variants

###  Outdoor

 Leads Outdoors. This is also the default (i.e., when no"
 Boundary is set)"



##### Full Specification
```json
{
	type: "Outdoor"
}
```


###  Ground

 The Surface is in contact with the Ground"



##### Full Specification
```json
{
	type: "Ground"
}
```


###  Space

 The Surface leads to another space whose temperature"
 and other properties are part of the simulation"
"
 Border conditions:"
 * **Solar Radiation**: As calculated by the Solar module"
 * **Net Shortwave (IR) Radiation**: Zero, for now at least (this is a good assumption if the surfaces inside the `Space` are at similar temperatures)"
 * **Convection Coefficient**: Indoor"
 * **Wind**: No"



##### Full Specification
```json
Boundary {
	type : "Space", // this should not change
	space : string
}
```

###  AmbientTemperature

 The surface leads to an environment with no wind or sun, and with a fixed"
 mean-radiant and dry bulb temperature"
"
 This object is useful for defining surfaces that lead to spaces that"
 we one is not interested in modelling; for example, a wall that separates"
 an apartment\'s room with the hall of the building. In that case, we don\'t"
 need to simulate the temperature of the hall... but we can assume a certain"
 temperature."
"
 Border conditions:"
 * **Solar Radiation**: None"
 * **Net Shortwave (IR) Radiation**: The set temperature"
 * **Convection Coefficient**: Indoor"
 * **Wind**: No"



##### Full Specification
```json
Boundary {
	type : "AmbientTemperature", // this should not change
	temperature : number
}
```

###  Adiabatic

 The temperature of the other side of the wall will be"
 the same as the one measured at the interior of the space"



##### Full Specification
```json
{
	type: "Adiabatic"
}
```


