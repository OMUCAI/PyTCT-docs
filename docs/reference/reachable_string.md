# reachable_string(G,m)

generate a string to the reachable state m

### Parameters
| Name       | Type    | Description   |  Default   |
|------------|---------|---------------|------------|
| `G`        | string  | name of DES   | *required* |
| `m`        | int     | state nnumber | *required* |



## Example

```python title="sample 1"
delta = [
    (0, 11, 1),
    (1, 12, 2),
    (2, 11, 0),
    (2, 14, 3)
]
Qm = [3]
pytct.create('G', 4, delta, Qm)

pytct.reachable_string('G',2)
```
