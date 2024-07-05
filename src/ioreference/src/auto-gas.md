# Gas

 Represents a Gas, as understood by the standard ISO-15099(2003)."
"
 ## Examples"
"
 #### `.spl`"
"
 ```json"
 {{#include ../../../model/tests/scanner/substance_gas.spl}}"
 ```"
"
 #### `.json`"
"
 ```json"
 {{#include ../../../model/tests/scanner/substance_gas.json}}"
 ```"


 ## Full Specification

```json
Gas {
   name : string,
   gas : GasSpecification, // optional,
}
```



#### name

 The name of the Substance. Should be unique for each"
 Substance in the Model object    "




#### gas (*optional*)

 A predefined gas"




