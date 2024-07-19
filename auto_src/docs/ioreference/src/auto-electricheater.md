# ElectricHeater

A simple model of an Electric Heater. It can only heat
and has a COP of 1. It only has two states: On/Off.

The thermostat that controls it—if any—is assumed to be in
the `target_space`

## Examples

#### `.spl`

```json
{{#include ../../../model/tests/scanner/hvac_electric_heater.spl}}
```

#### `.json`

```json
{{#include ../../../model/tests/scanner/hvac_electric_heater.json}}
```


 ## Full Specification

```json
ElectricHeater {
   name : string,
   target_space : string, // optional,
   max_heating_power : number, // optional,
   heating_setpoint : number, // optional,
}
```



#### name

The name of the system




#### target_space (*optional*)

The `Space` that this [`ElectricHeater`] heats and/or
cools




#### max_heating_power (*optional*)

Max heating power




#### heating_setpoint (*optional*)

The temperature that triggers the on/off option.

This tempareture is \'measured\' in the `target_space`. If
the dry bulb tempreature in the `target_space` is below
this value, the heater starts heating.

> Note: This assumes automatic control; that is to say, this
condition will be evaluated every timestep of the heat model
simulation (as opposed to the occupant/people control timestep,
which is the one set by the user witht the simulation options)








## API

The following properties are available for simulating control algorithms

| Property | Getter | Setter |
|----------|--------|--------|
| `power_consumption` | Yes   | Yes |