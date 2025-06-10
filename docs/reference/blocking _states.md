# blocking _states(DES)

generate all blocking states in DES

### Parameters
| Name       | Type    | Description                                                          |  Default   |
|------------|---------|----------------------------------------------------------------------|------------|
| `DAT`      | string  | name of the blocking data for the DES.                               | *required* |
| `DES`      | string  | name of the DES.                                                     | *required* |


## Example

```python title="sample 1"

delta = [
    (0, 11, 1),
    (1, 12, 2),
    (2, 11, 0),
    (2, 14, 3)
]
Qm = [0]
pytct.create('DES', 4, delta, Qm)


pytct.blocking_states('DES')

```
