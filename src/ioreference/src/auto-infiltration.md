# Infiltration

 Infiltration is the unintended air exchange between an interior"
 space and the exterior. In `SIMPLE`, infiltrations are added to the"
 intended ventilation."
"
 This group of objects allow defining infiltration"
 on different ways. Which variety is better will depend on the"
 information available and the kind of building."
"
 ## Examples"
"
 #### `.spl`"
 ```json"
 // Note that Infiltration is always attached to a Space"
 {{#include ../../../model/tests/box.spl:bedroom}}"
 ```"
"
 #### `.json`"
 ```json"
 {{#include ../../../model/tests/scanner/infiltration_design_flow_rate.json}}"
 ```"
"
 ```json"
 {{#include ../../../model/tests/scanner/infiltration_constant.json}}"
 ```"
 > **Note**: This object cannot be declared by itself in a `SIMPLE` model,"
 as it is always embeded on a `Space`"


 ## Supported Variants

###  Constant

 A contant infiltration, specified in `m3/s`"



##### Full Specification
```json
Infiltration {
	type : "Constant", // this should not change
	flow : number
}
```

###  Blast

 It is the same as the `DesignFlowRate` infiltration object,"
 but specifying the  default values from BLAST, as described"
 in the EnergyPlus\' Input Output reference"



##### Full Specification
```json
Infiltration {
	type : "Blast", // this should not change
	flow : number
}
```

###  Doe2

 It is the same as the `DesignFlowRate` infiltration object,"
 but specifying the default values from DOE-2 as described"
 in the EnergyPlus\' Input Output reference"



##### Full Specification
```json
Infiltration {
	type : "Doe2", // this should not change
	flow : number
}
```

###  DesignFlowRate

 Sets the infiltration to the `DesignFlowRate` values using an"
 arbitrary set of values. This option is based on EnergyPlus\'"
 object of the same name."
"
"
 The flow $\\phi$ (in $m^3/s$) is calculated from the parameters"
 $A$, $B$, $C$, $D$ and $\\phi_{design}$ as follows:"
"
 $$ \\phi = \\phi_{design} (A + B|T_{space} - T_{outside}| + C\\times W_{speed} + D\\times W^2_{speed})$$"
"
 The inputs to this object are $A$, $B$, $C$, $D$, $\\phi_{design}$ ."



##### Full Specification
```json
Infiltration {
	type : "DesignFlowRate", // this should not change
	a : number
	b : number,
	c : number,
	d : number,
	phi : number,
}
```

###  EffectiveAirLeakageArea

 Sets the infiltration based on `EffectiveLeakageArea` as"
 described in the EnergyPlus\' Input Output reference. This"
 variant of infiltration requires the space to be part of a"
 `Building`"
     "
 The infiltration rate—in $m^3/s$—is calculated based on the"
 following equation:"
"
 $$ \\phi = \\frac{A_L}{1000} \\sqrt{C_s \\Delta T + C_w W^2_{speed}}$$"
"
 where:"
 * $A_L$ is the effective air leakage in $cm^2$ @ 4Pa (**NOTE THAT THE INPUT IS IN M2**)"
 * $C_s$ is the coefficient for stack induced infiltration"
 * $C_w$ is the coefficient for wind induced infiltration"
"
 **The only input to this object is the effecctive air leakage, $A_L$, in $cm^2$ @ 4Pa**."
 The other parameters—$C_s$ and $C_w$—are derived based"
 on the required `Building` object associated with the `Space` that owns"
 this `Infiltration`. For this to work, the associated `Building` needs"
 to have been assigned the fields `n_storeys` and a `shelter_class`"
 (which allow calculating $C_s$ and $C_w$) OR the properties of"
 `stack_coefficient` (i.e., $C_s$) and `wind_coefficient` (i.e., $C_w$)."
"
 > **Note:** The `EffectiveAirLeakageArea` object is appropriate for buildings"
 > of 3 storeys or less."
"
 ## Example"
"
 ```json"
 {{#include ../../../model/tests/cold_wellington_apartment.spl:building}}"
"
 {{#include ../../../model/tests/cold_wellington_apartment.spl:kids_bedroom}}"
 ```"
"
 ### Values for $A_L$"
"
 *(source of this example: Sherman and Grimsrud (1980) Infiltration-Pressurization correlation: Simplified physical modeling). Conference of American Society of Heating, Refrigeration and Air Conditioning Engineers*"
"
 Ideally, the value from $A_L$ should come from a blower-door test. When doing one of these,"
 you can get a table like the following:"
"
 | Q ($m^3/s$) | $\\Delta P$ ($Pa$) |"
 ------|------------------------------"
 | 10 | 0.222 |"
 | 20 | 0.338 |"
 | 30 | 0.433 |"
 | 40 | 0.513 |"
 | 50 | 0.586 |"
"
 This data can be fitted in a model with the shape:"
"
 $$ Q = K {\\Delta P}^b$$"
"
 In this case, the values for $K$ and $b$ are $0.0555$ and $0.6032$, respectively."
"
 Evaluating this model at $4 Pa$, we get an air flow $Q$ of $0.128 m^3/s$."
"
 To calculate $A_L$ we now need to use this data in the following equation, which relates"
 air flows through openings of size $A_L$:"
"
 $$ Q = A_L \\sqrt{\\frac{2 \\Delta P}{\\rho}} $$"
"
 Where $\\rho$ is the air density of $1.2 kg/m^3$. So, the estimated $A_L$ would be $0.0496 m^2$"



##### Full Specification
```json
Infiltration {
	type : "EffectiveAirLeakageArea", // this should not change
	area : number
}
```

