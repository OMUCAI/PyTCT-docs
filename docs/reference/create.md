# create(G, statenum, trans, marker)

creates an automaton model (.DES file)

### Parameters
| Name         | Type      | Description               | Default    |
|--------------|-----------|---------------------------|------------|
| `G`          | string    | name of output automaton  | *required* |
| `statenum`   | int       | number of states          | *required* |
| `trans`      | TransList | list of transition tuples.<br>For more information, please see [TransList Type](#translist-type).| *required* |
| `marker`     | list      | list of marker states     | *required* |


### TransList Type

There are several ways to write a Transition Tuple.

1. Number only (Classic TCT)

    `(exit state: int, event: int, enter_state: int)`

    !!! note
        Odd number event is controllable and even number event is uncontrollable.

    ```python
    trans: TransList = [
        (0, 11, 1),
        (1, 10, 0),
        (1, 12, 2),
    ]
    ```

2. String Event (PyTCT Original)

    `(exit state: int, event: string, enter_state: int, 'u'[uncontrollable] or 'c'[controllable])`

    !!! note
        String events and int events cannot be mixed.

    ```python
    trans: TransList = [
        (0, 'run', 1, 'c'),
        (1, 'finish', 0, 'u'),
        (1, 'broken', 2, 'u'),
    ]
    ```

3. String State (PyTCT Original)
    
    `(exit state: string, event: string, enter_state: string, 'u'[uncontrollable] or 'c'[controllable])`

    !!! note
        it will not be able to be displayed on AutomatonDisplay after processing such as sync.
    
    ```python
    trans: TransList = [
        ('idle', 'run', 'working', 'c'),
        ('working', 'finish', 'idle', 'u'),
        ('working', 'broken', 'repairing', 'u'),
    ]
    ```

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
pytct.create("model", 4, delta, Qm)
```

```python title="sample 2"
delta = [
    (0, "run", 1, "c"),
    (1, "finish", 0, "u"),
    (1, "broken", 2, "u"),
    (2, "repaired", 0, "c"),
    (0, "sold", 3, "c")
]
Qm = [0,1]
pytct.create("model", 4, delta, Qm)
```

```python title="sample 3"
delta = [
    ("idle", "run", "running", "c"),
    ("running", "finish", "idle", "u"),
    ("running", "broken", "broken", "u"),
    ("broken", "repaired", "idle", "c"),
    ("idle", "sold", "sold", "c")
]
Qm = ["idle", "running"]
pytct.create("model", 4, delta, Qm)
```
