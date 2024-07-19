# Construction

An object representing an array of
Materials, ordered from front to back

Front and back can be indoor, outdoor, or they can both be
indoor (it depends exclusively on the `Boundary` set to the
surface)


 ## Examples

#### `.spl`
```rs
{{#include ../../../model/tests/scanner/construction.spl}}
```
#### `.json`
```rs
{{#include ../../../model/tests/scanner/construction.json}}
```


 ## Full Specification

```json
Construction {
   name : string,
   materials : [string, ...],
}
```



#### name

The name of the Construction object.
Must be unique within the model




#### materials

The indices of the Material objects in the
materials property of the Model object




