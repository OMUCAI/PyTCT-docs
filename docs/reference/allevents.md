# allevent(ALL, DES1)

creates one-state DES selfloop with all the events of DES1

### Parameters
| Name       | Type    | Description                                              |  Default   |
|------------|---------|----------------------------------------------------------|------------|
| `ALL`      | string  | name of one-state DES selfloop with all the event of DES1| *required* |
| `DES1`     | string  | name of DES1                                             | *required* |


## Example

```python title="sample 1"
delta = [
    (0, 11, 1),
    (1, 10, 0)
]
Qm = [0]
pytct.create("model", 2, delta, Qm)

pytct.allevents("ALL", "model")

```

```python title="sample 2"
delta = [
    (0, 11, 1),
    (1, 12, 2),
    (2, 11, 0),
    (2, 14, 3)
]
Qm = [0, 3]
pytct.create("model", 4, delta, Qm)

pytct.allevents("ALL", "model")
```