# Material

 The representation of a physical layer-Material."
 That is to say, a layer of a certain thickness"
 made of a certain Substance"
"
 ## Examples"
"
 ##### `.spl`"
 ```json"
 {{#include ../../../model/tests/scanner/material.spl}}"
 ```"
"
 ##### `.json`"
 ```json"
 {{#include ../../../model/tests/scanner/material.json}}"
 ```"


 ## Full Specification

```json
Material {
   name : string,
   substance : string,
   thickness : number,
}
```



#### name

 The name of the material object"




#### substance

 The name of the `Substance` of which this"
 [`Material`] is made of    "




#### thickness

 The thickness of the [`Material`]"




