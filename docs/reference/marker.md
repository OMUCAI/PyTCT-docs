# marker(name)

returns the list of marker states of DES 

### Parameters
| Name       | Type    | Description |  Default   |
|------------|---------|-------------|------------|
| `name`     | string  | name of DES | *required* |



## Example

```python title="sample 1"
delta = [
    (0, 11, 1),
    (1, 12, 2),
    (2, 11, 0),
    (2, 14, 3)
]
Qm = [3]
pytct.create("model", 4, delta, Qm)

pytct.marker("model")
```
