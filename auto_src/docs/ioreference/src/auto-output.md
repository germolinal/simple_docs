# Output

 Possible outputs to request from the simulation
 
 ## Example
 
 ```json
 {{ #include ../../../model/tests/box.spl:bedroom }}
 
 {{ #include ../../../model/tests/box.spl:bedroom_output }}
 ```
 


 ## Supported Variants

###  Clothing

 The amount of clothing the person is using,
 in Clo value



```rs
Output {
	Clothing : string
}
```

###  FenestrationOpenFraction

 Represents how open is a fenestration.
 Contains the Index of fenestration, and its open fraction



```rs
Output {
	FenestrationOpenFraction : string
}
```

###  HeatingCoolingPowerConsumption

 Represents the heating/cooling energy consumption of a Heating/Cooling system,
 in Watts
 
 Contains the index of the HVAC in the building\\'s vector,
 and the power.



```rs
Output {
	HeatingCoolingPowerConsumption : string
}
```

###  LuminairePowerConsumption

 Represents the power being consumed by
 a Luminaire object, in Watts (luminaire index, power)



```rs
Output {
	LuminairePowerConsumption : string
}
```

###  SurfaceFrontConvectionCoefficient

 The convective heat transfer coefficient
 at the front of a surface



```rs
Output {
	SurfaceFrontConvectionCoefficient : string
}
```

###  SurfaceBackConvectionCoefficient

 The convective heat transfer coefficient
 at the back of a surface



```rs
Output {
	SurfaceBackConvectionCoefficient : string
}
```

###  SurfaceFrontConvectiveHeatFlow

 The convective heat flow
 at the front of a surface



```rs
Output {
	SurfaceFrontConvectiveHeatFlow : string
}
```

###  SurfaceBackConvectiveHeatFlow

 The convective heat flow
 at the back of a surface



```rs
Output {
	SurfaceBackConvectiveHeatFlow : string
}
```

###  SurfaceFrontSolarIrradiance

 Incident solar irradiance at the front



```rs
Output {
	SurfaceFrontSolarIrradiance : string
}
```

###  SurfaceBackSolarIrradiance

 Incident solar irradiance at the back



```rs
Output {
	SurfaceBackSolarIrradiance : string
}
```

###  SurfaceFrontIRIrradiance

 Incident Infrared irradiance at the front



```rs
Output {
	SurfaceFrontIRIrradiance : string
}
```

###  SurfaceBackIRIrradiance

 Incident Infrared irradiance at the back



```rs
Output {
	SurfaceBackIRIrradiance : string
}
```

###  FenestrationFrontConvectionCoefficient

 The convective heat transfer coefficient
 at the front of a surface



```rs
Output {
	FenestrationFrontConvectionCoefficient : string
}
```

###  FenestrationBackConvectionCoefficient

 The convective heat transfer coefficient
 at the back of a surface



```rs
Output {
	FenestrationBackConvectionCoefficient : string
}
```

###  FenestrationFrontConvectiveHeatFlow

 The convective heat flow
 at the front of a surface



```rs
Output {
	FenestrationFrontConvectiveHeatFlow : string
}
```

###  FenestrationBackConvectiveHeatFlow

 The convective heat flow
 at the back of a surface



```rs
Output {
	FenestrationBackConvectiveHeatFlow : string
}
```

###  FenestrationFrontSolarIrradiance

 Incident solar irradiance at the front



```rs
Output {
	FenestrationFrontSolarIrradiance : string
}
```

###  FenestrationBackSolarIrradiance

 Incident solar irradiance at the back



```rs
Output {
	FenestrationBackSolarIrradiance : string
}
```

###  FenestrationFrontIRIrradiance

 Incident Infrared irradiance at the front



```rs
Output {
	FenestrationFrontIRIrradiance : string
}
```

###  FenestrationBackIRIrradiance

 Incident Infrared irradiance at the back



```rs
Output {
	FenestrationBackIRIrradiance : string
}
```

###  SpaceDryBulbTemperature

 Space Air Temperature in C... The elements
 are the index of the Space in the Building mode
 and the temperature



```rs
Output {
	SpaceDryBulbTemperature : string
}
```

###  SpaceInfiltrationVolume

 The volume of air that is entering the space in
 an uncontrolled way. In m3/s



```rs
Output {
	SpaceInfiltrationVolume : string
}
```

###  SpaceInfiltrationTemperature

 The temperature of air that is entering the space in
 an uncontrolled way. In C



```rs
Output {
	SpaceInfiltrationTemperature : string
}
```

###  SpaceVentilationVolume

 The volume of air that is entering the space in
 a controlled way. In m3/s



```rs
Output {
	SpaceVentilationVolume : string
}
```

###  SpaceVentilationTemperature

 The temperature of air that is entering the space in
 a controlled way. In C



```rs
Output {
	SpaceVentilationTemperature : string
}
```

###  SpaceAirExchangeVolume

 The volume of air that is moving from one space to another in
 a controlled way. In m3/s



```rs
Output {
	SpaceAirExchangeVolume : string
}
```

###  SurfaceNodeTemperature

 Temperature (Float) of Surface\\'s (usize) node (usize)
 I.e. the order is (Surface Index, Node index, Temperature).



```rs
Output {
	SurfaceNodeTemperature : string
}
```

###  FenestrationNodeTemperature

 Temperature (Float) of Fenestration\\'s (usize) node (usize)
 I.e. the order is (Surface Index, Node index, Temperature).



```rs
Output {
	FenestrationNodeTemperature : string
}
```

