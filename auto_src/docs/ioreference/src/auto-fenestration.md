# Fenestration

A surface that can potentially be opened and closed.
It can be of any Construction and it does not need to be
a hole in another surface.

## Examples

#### `.spl`
```json
{{#include ../../../model/tests/scanner/fenestration.spl}}
```

#### `.json`
```json
{{#include ../../../model/tests/scanner/fenestration.json}}
```


 ## Full Specification

```json
Fenestration {
   name : string,
   vertices : Polygon3D,
   construction : string,
   category : FenestrationType,
   operation : FenestrationPosition, // optional,
   front_boundary : Boundary,
   back_boundary : Boundary,
   precalculated_front_convection_coef : number, // optional,
   precalculated_back_convection_coef : number, // optional,
   parent_surface : string, // optional,
}
```



#### name

The name of the sub surface




#### vertices

An array of Numbers representing the vertices of the
surface. The length of this array must be divisible by 3.




#### construction

The name of the Construction object in the
constructions property of the Model object    




#### category

Defines whether a `Fenestration` is a Window, Door, or other.
If none is given, the assumed behaviour is that it is a Window.




#### operation (*optional*)

The opportunity for operating the Fenestration.
If none is given, the window is assumed to be Fixed
at Closed position.




#### front_boundary

The front Boundary. No boundary means it leads to the
exterior




#### back_boundary

The back Boundary. No boundary means it leads to the
exterior




#### precalculated_front_convection_coef (*optional*)

The front convection coefficient, in `W/m2K`

This value fixes the value, so the automatic calculations
in SIMPLE have no effect.




#### precalculated_back_convection_coef (*optional*)

The back convection coefficient, in `W/m2K`

This value fixes the value, so the automatic calculations
in SIMPLE have no effect.




#### parent_surface (*optional*)

The name of the surface containing this `Fenestration`,
if any. A hole will be made in the parent surface in order
to accomodate

Note that a `Fenestration` can be self contained (i.e., it can have
no parent surface), which allows representing situation where
the fenestration is very large and therefore there would be no area
for wall.

> Note: This field will not be serialized. This is beacuse there is
no quarantee that the `surfaces` will be there before the `fenestrations`
and thus there would be errors when deserializing. In any case, it is assumed that
JSON models are read/written by machines—e.g., either by
serializing a Model or by another kind of machine—and therefore
the convenience of not having to write down the vertices around
holes is not much needed.






## API Access

```rs
// by name
let my_fenestration = fenestration(string);
// by index
let my_fenestration = fenestration(int);
```



## API

The following properties are available for simulating control algorithms

| Property | Getter | Setter |
|----------|--------|--------|
| `front_temperature` | Yes   | Research mode |
| `back_temperature` | Yes   | Research mode |
| `open_fraction` | Yes   | Yes |
| `front_convection_coefficient` | Yes   | Research mode |
| `back_convection_coefficient` | Yes   | Research mode |
| `front_convective_heat_flow` | Yes   | Research mode |
| `back_convective_heat_flow` | Yes   | Research mode |
| `front_incident_solar_irradiance` | Yes   | Research mode |
| `back_incident_solar_irradiance` | Yes   | Research mode |
| `front_ir_irradiance` | Yes   | Research mode |
| `back_ir_irradiance` | Yes   | Research mode |