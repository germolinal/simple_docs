# IdealHeaterCooler

An ideal Heating and Cooling device, with a COP of 1.

It only has two states: On/Off.

## Example

#### `.spl`

```json
{{#include ../../../model/tests/scanner/hvac_ideal_heater_cooler.spl}}
```

#### `.json`

```json
{{#include ../../../model/tests/scanner/hvac_ideal_heater_cooler.json}}
```


 ## Full Specification

```json
IdealHeaterCooler {
   name : string,
   target_space : string, // optional,
   max_heating_power : number, // optional,
   max_cooling_power : number, // optional,
   heating_setpoint : number, // optional,
   cooling_setpoint : number, // optional,
}
```



#### name

The name of the system




#### target_space (*optional*)

The `Space`s that this `IdealHeaterCooler` heats and/or
cools




#### max_heating_power (*optional*)

Max heating power




#### max_cooling_power (*optional*)

Max cooling power




#### heating_setpoint (*optional*)

The temperature that automatically triggers the on/off option.

This tempareture is \'measured\' in the `thermostat_location`. If
the dry bulb tempreature in the `thermostat_location` is below
this value, the system starts heating.

> Note: This assumes automatic control; that is to say, this
condition will be evaluated every timestep of the heat model
simulation (as opposed to the occupant/people control timestep,
which is the one set by the user witht the simulation options)




#### cooling_setpoint (*optional*)

The temperature that triggers the on/off option.

This tempareture is \'measured\' in the `thermostat_location`. If
the dry bulb tempreature in the `thermostat_location` is over
this value, the system starts cooling.

> Note: This assumes automatic control; that is to say, this
condition will be evaluated every timestep of the heat model
simulation (as opposed to the occupant/people control timestep,
which is the one set by the user witht the simulation options)








## API

The following properties are available for simulating control algorithms

| Property |
|----------|
| `power_consumption` |  