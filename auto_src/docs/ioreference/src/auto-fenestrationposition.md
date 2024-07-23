# FenestrationPosition

Defines whether the Fenestration is fixed or openable.

## Example

#### `.json`
```json
{{#include ../../../model/tests/scanner/fenestration_position.json}}
```

> **Note**: This object cannot be declared by itself in a `SIMPLE` model,
as it is always embeded on a `Fenestration` object



 ## Supported Variants

###  Fixed

It is fixed at a certain open fraction



##### Full Specification
```json
FenestrationPosition {
	type : "Fixed", // this should not change
	fraction : number, // optional
}
```

###  Continuous

It can be position at any position, from fully opened to fully closed



##### Full Specification
```json
FenestrationPosition {
	type : "Continuous", // this should not change
	max : number, // optional
	min : number, // optional,
}
```

###  Binary

It can only be opened or closed, no in-between



##### Full Specification
```json
FenestrationPosition {
	type : "Binary", // this should not change
	open : number, // optional
	closed : number, // optional,
}
```

