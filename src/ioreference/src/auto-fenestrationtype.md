# FenestrationType

 Defines whether the fenestration is a Door or a Window."
"
 At present, this option has no effect whatsoever"
"
 ## Example"
"
 #### `.json`"
 ```json"
 {{#include ../../../model/tests/scanner/fenestration_type.json}}"
 ```"
"
 > **Note**: This object cannot be declared by itself in a `SIMPLE` model,"
 as it is always embeded on a `Fenestration` object"
"


 ## Supported Variants

###  Window

 This is a Window. This is the default."



##### Full Specification
```json
"Window"
```

###  Door

 This is a Door"



##### Full Specification
```json
"Door"
```

###  Opening

 This is an opening, meaning that it lets air through it."



##### Full Specification
```json
"Opening"
```

