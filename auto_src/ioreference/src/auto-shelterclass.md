# ShelterClass

 Indicates how sheltered is the building. This affects its infiltration"
  "
 ## Examples"
"
 #### `.json`"
"
 ```json"
 {{#include ../../../model/tests/scanner/shelter_class.json}}"
 ```"
 > **Note**: This object cannot be declared by itself in a `SIMPLE` model,"
 as it is always embeded on a `Building` object"


 ## Supported Variants

###  NoObstructions

 No obstructions or local shielding"



##### Full Specification
```json
"NoObstructions"
```

###  IsolatedRural

 Typical shelter for an isolated rural house"



##### Full Specification
```json
"IsolatedRural"
```

###  Urban

 Typical shelter caused by other buildings across the street"



##### Full Specification
```json
"Urban"
```

###  LargeLotUrban

 Typical shelter for urban buildings on larger lots"



##### Full Specification
```json
"LargeLotUrban"
```

###  SmallLotUrban

 Typical shelter produced by buildings that are immediately adjacent."



##### Full Specification
```json
"SmallLotUrban"
```

