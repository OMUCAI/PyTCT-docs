# reachable_string(name,m)

generate a string to the reachable state m

### Parameters
| Name       | Type    | Description   |  Default   |
|------------|---------|---------------|------------|
| `name`     | string  | name of DES   | *required* |
| `m`        | string  | state nnumber | *required* |



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

pytct.reachable_string('model',2)
```
