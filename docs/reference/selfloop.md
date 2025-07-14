## pytct.selfloop(G_SL,G,[event1,event2,...])

selfloop G with events event1,event2,......

### Parameters
| Name         | Type      | Description                            | Default    |
|--------------|-----------|----------------------------------------|------------|
| `G_SL`       | string    | name of output automaton               | *required* |
| `G`          | string    | name of automaton                      | *required* |
| `[event1,event2,...]`  | EventList | list of events               | *required* |


## Example

```python title="sample 1"
delta = [
    (0, 11, 1),
    (1, 10, 0),
    (1, 12, 2),
    (2, 13, 0),
    (0, 15, 3)
]
Qm = [0, 1]
pytct.create('G', 4, delta, Qm)

pytct.selfloop('G_SL','G',['11,13'])

```
