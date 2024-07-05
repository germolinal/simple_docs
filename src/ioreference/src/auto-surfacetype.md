# SurfaceType

 The kind of surface, useful for pre- and post-processing."
"
 This information does not affect the simulation outcome."
 For example, `SIMPLE` will decide whether a wall is interior"
 or exterior based on the boundaries, and will not check these"
 labels. However, these labels can be useful for creating"
 measures (e.g., insulate all the exterior walls)"
"
 # Example"
"
 #### `.json`"
 ```json"
 {{#include ../../../model/tests/scanner/surface_type.json}}"
 ```"
"


 ## Supported Variants

###  ExteriorWall

 A Wall that connects a space with the exterior.    "



##### Full Specification
```json
"ExteriorWall"
```

###  InteriorWall

 A Wall connecting two spaces"



##### Full Specification
```json
"InteriorWall"
```

###  GroundFloor

 A useful horizontal surface that touches the ground"



##### Full Specification
```json
"GroundFloor"
```

###  ExteriorFloor

 A floor that leads to the exterior (e.g., a floor"
 suspended by columns)"



##### Full Specification
```json
"ExteriorFloor"
```

###  InteriorFloor

 Floor/ceiling that connects two spaces, and whose area is part of the  "
 building or project being modelled. For instance, the top ceiling of an"
 apartment is often, strictly speaking, an interior floor... but it is"
 not part of the sellable area of the apartment itself"



##### Full Specification
```json
"InteriorFloor"
```

###  Ceiling

 A floor/ceiling that connect two spaces, but whose area is not part"
 of the area of the project/building (see the `InteriorFloor` variant)."



##### Full Specification
```json
"Ceiling"
```

###  Roof

 A surfaces at the top of a building"



##### Full Specification
```json
"Roof"
```

###  Other

 Other kind of surface"



##### Full Specification
```json
"Other"
```

