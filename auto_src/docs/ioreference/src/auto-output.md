# Output

ossible outputs to request from the simulation

# Example

``json
{#include ../../../model/tests/box.spl:bedroom}}
{#include ../../../model/tests/box.spl:bedroom_output}}
``



 ## Supported Variants

###  Clothing

he amount of clothing the person is using,
n Clo value



```rs
Output {
	Clothing : string
}
```

###  FenestrationOpenFraction

epresents how open is a fenestration.
ontains the Index of fenestration, and its open fraction



```rs
Output {
	FenestrationOpenFraction : string
}
```

###  HeatingCoolingPowerConsumption

epresents the heating/cooling energy consumption of a Heating/Cooling system,
n Watts

ontains the index of the HVAC in the building\\'s vector,
nd the power.



```rs
Output {
	HeatingCoolingPowerConsumption : string
}
```

###  LuminairePowerConsumption

epresents the power being consumed by
 Luminaire object, in Watts (luminaire index, power)



```rs
Output {
	LuminairePowerConsumption : string
}
```

###  SurfaceFrontConvectionCoefficient

he convective heat transfer coefficient
t the front of a surface



```rs
Output {
	SurfaceFrontConvectionCoefficient : string
}
```

###  SurfaceBackConvectionCoefficient

he convective heat transfer coefficient
t the back of a surface



```rs
Output {
	SurfaceBackConvectionCoefficient : string
}
```

###  SurfaceFrontConvectiveHeatFlow

he convective heat flow
t the front of a surface



```rs
Output {
	SurfaceFrontConvectiveHeatFlow : string
}
```

###  SurfaceBackConvectiveHeatFlow

he convective heat flow
t the back of a surface



```rs
Output {
	SurfaceBackConvectiveHeatFlow : string
}
```

###  SurfaceFrontSolarIrradiance

ncident solar irradiance at the front



```rs
Output {
	SurfaceFrontSolarIrradiance : string
}
```

###  SurfaceBackSolarIrradiance

ncident solar irradiance at the back



```rs
Output {
	SurfaceBackSolarIrradiance : string
}
```

###  SurfaceFrontIRIrradiance

ncident Infrared irradiance at the front



```rs
Output {
	SurfaceFrontIRIrradiance : string
}
```

###  SurfaceBackIRIrradiance

ncident Infrared irradiance at the back



```rs
Output {
	SurfaceBackIRIrradiance : string
}
```

###  FenestrationFrontConvectionCoefficient

he convective heat transfer coefficient
t the front of a surface



```rs
Output {
	FenestrationFrontConvectionCoefficient : string
}
```

###  FenestrationBackConvectionCoefficient

he convective heat transfer coefficient
t the back of a surface



```rs
Output {
	FenestrationBackConvectionCoefficient : string
}
```

###  FenestrationFrontConvectiveHeatFlow

he convective heat flow
t the front of a surface



```rs
Output {
	FenestrationFrontConvectiveHeatFlow : string
}
```

###  FenestrationBackConvectiveHeatFlow

he convective heat flow
t the back of a surface



```rs
Output {
	FenestrationBackConvectiveHeatFlow : string
}
```

###  FenestrationFrontSolarIrradiance

ncident solar irradiance at the front



```rs
Output {
	FenestrationFrontSolarIrradiance : string
}
```

###  FenestrationBackSolarIrradiance

ncident solar irradiance at the back



```rs
Output {
	FenestrationBackSolarIrradiance : string
}
```

###  FenestrationFrontIRIrradiance

ncident Infrared irradiance at the front



```rs
Output {
	FenestrationFrontIRIrradiance : string
}
```

###  FenestrationBackIRIrradiance

ncident Infrared irradiance at the back



```rs
Output {
	FenestrationBackIRIrradiance : string
}
```

###  SpaceDryBulbTemperature

pace Air Temperature in C... The elements
re the index of the Space in the Building mode
nd the temperature



```rs
Output {
	SpaceDryBulbTemperature : string
}
```

###  SpaceInfiltrationVolume

he volume of air that is entering the space in
n uncontrolled way. In m3/s



```rs
Output {
	SpaceInfiltrationVolume : string
}
```

###  SpaceInfiltrationTemperature

he temperature of air that is entering the space in
n uncontrolled way. In C



```rs
Output {
	SpaceInfiltrationTemperature : string
}
```

###  SpaceVentilationVolume

he volume of air that is entering the space in
 controlled way. In m3/s



```rs
Output {
	SpaceVentilationVolume : string
}
```

###  SpaceVentilationTemperature

he temperature of air that is entering the space in
 controlled way. In C



```rs
Output {
	SpaceVentilationTemperature : string
}
```

###  SpaceAirExchangeVolume

he volume of air that is moving from one space to another in
 controlled way. In m3/s



```rs
Output {
	SpaceAirExchangeVolume : string
}
```

###  SurfaceNodeTemperature

emperature (Float) of Surface\\'s (usize) node (usize)
.e. the order is (Surface Index, Node index, Temperature).



```rs
Output {
	SurfaceNodeTemperature : string
}
```

###  FenestrationNodeTemperature

emperature (Float) of Fenestration\\'s (usize) node (usize)
.e. the order is (Surface Index, Node index, Temperature).



```rs
Output {
	FenestrationNodeTemperature : string
}
```

