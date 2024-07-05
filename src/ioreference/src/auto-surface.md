# Surface

 A fixed (i.e., not movable) surface in the building (or surroundings). This can be of"
 any Construction, transparent or not."
"
 ## Examples"
"
 #### `.spl`"
 ```json"
 {{#include ../../../model/tests/scanner/surface.spl}}"
 ```"
 #### `.json`"
 ```json"
 {{#include ../../../model/tests/scanner/surface.json}}"
 ```"


 ## Full Specification

```json
Surface {
   name : string,
   vertices : Polygon3D,
   construction : string,
   front_boundary : Boundary,
   back_boundary : Boundary,
   category : SurfaceType, // optional,
   precalculated_front_convection_coef : number, // optional,
   precalculated_back_convection_coef : number, // optional,
}
```



#### name

 The name of the surface"




#### vertices

 An array of Numbers representing the vertices of the"
 surface. The length of this array must be divisible by 3."




#### construction

 The name of the construction in the Model\'s"
 Construction array    "




#### front_boundary

 The Boundary in front of the Surface"




#### back_boundary

 The Boundary in back of the Surface"




#### category (*optional*)

 The Surface Category."
"
 This field does not affect the simulations, as"
 it was designed to be used based on conventions (see"
 [`SurfaceType`] documentation). So, if no [`SurfaceType`]"
 is assigned, we cannot tell you what to do."




#### precalculated_front_convection_coef (*optional*)

 The front convection coefficient, in `W/m2K`"
"
 This value fixes the value, so the automatic calculations"
 in SIMPLE have no effect."




#### precalculated_back_convection_coef (*optional*)

 The back convection coefficient, in `W/m2K`"
"
 This value fixes the value, so the automatic calculations"
 in SIMPLE have no effect."






## API Access

```rs
// by name
let my_surface = surface(string);
// by index
let my_surface = surface(int);
```



## API

The following properties are available for simulating control algorithms

| Property | Getter | Setter |
|----------|--------|--------|
| `front_temperature` | Yes   | Research mode |
| `back_temperature` | Yes   | Research mode |
| `front_convection_coefficient` | Yes   | Research mode |
| `back_convection_coefficient` | Yes   | Research mode |
| `front_convective_heat_flow` | Yes   | Research mode |
| `back_convective_heat_flow` | Yes   | Research mode |
| `front_incident_solar_irradiance` | Yes   | Research mode |
| `back_incident_solar_irradiance` | Yes   | Research mode |
| `front_ir_irradiance` | Yes   | Research mode |
| `back_ir_irradiance` | Yes   | Research mode |