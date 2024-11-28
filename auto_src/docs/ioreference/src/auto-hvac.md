# HVAC

A collection of elements heating and cooling systems

## Example `.spl`

```json
{{ #include ../../../model/tests/scanner/hvac_electric_heater.spl }}

```

## Example `.json`

```json
{{ #include ../../../model/tests//scanner/hvac_electric_heater.json }}

```



 ## Supported Types

* **IdealHeaterCooler**: An ideal heating/cooling device.
Heats and Cools with an efficiency of
1, and nothing effects its COP or efficiency    

* **ElectricHeater**: An electric heater, it can only
heat.



## API Access

```rs
// by name
let my_hvac = hvac(string);
// by index
let my_hvac = hvac(int);
```
