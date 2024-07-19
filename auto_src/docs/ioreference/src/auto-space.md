# Space

Represents a space with homogeneous temperature within a building. It is often actual room enclosed by walls, but it can also
be more than one room. In this latter case, there will be walls
within the Space, meaning that there are walls whose Front and Back
boundary is this space.

## Examples

#### `.spl`
```rs
{{#include ../../../model/tests/scanner/space.spl}}
```
#### `.json`
```rs
{{#include ../../../model/tests/scanner/space.json}}
```


 ## Full Specification

```json
Space {
   name : string,
   volume : number, // optional,
   infiltration : Infiltration, // optional,
   building : string, // optional,
   storey : int, // optional,
   purposes : [SpacePurpose, ...],
}
```



#### name

The name of the space




#### volume (*optional*)

Volume of the space




#### infiltration (*optional*)

The infiltration in the space




#### building (*optional*)

The building in which this `Space` is inserted




#### storey (*optional*)

The storey in which the space is located,
indexing from 0 (i.e., ground floor is 0)




#### purposes

The purposes in a room. It can have multiple
purposes (e.g., a Living/Dining/Kithen space)






## API Access

```rs
// by name
let my_space = space(string);
// by index
let my_space = space(int);
```



## API

The following properties are available for simulating control algorithms

| Property | Getter | Setter |
|----------|--------|--------|
| `dry_bulb_temperature` | Yes   | Research mode |
| `brightness` | Yes   | Research mode |
| `loudness` | Yes   | Research mode |
| `infiltration_volume` | Yes   | Research mode |
| `infiltration_temperature` | Yes   | Research mode |
| `ventilation_volume` | Yes   | Research mode |
| `ventilation_temperature` | Yes   | Research mode |