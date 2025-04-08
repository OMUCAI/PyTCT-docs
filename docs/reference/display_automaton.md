# display_automaton(name: string \[, convert: bool, color: bool\]) -&gt; AutomatonDisplay

Get AutomatonDisplay instance and display automaton.

test

#### Parameter

| Name      | Type   | Description                                                                         | Default    |
| --------- | ------ | ----------------------------------------------------------------------------------- | ---------- |
| `name`    | string | DES model name                                                                      | _required_ |
| `convert` | bool   | Apply and display String Event and String State                                     | `True`     |
| `color`   | bool   | Separate colors depending on whether the control is uncontrollable or controllable. | `False`    |

## Return

[AutomatonDisplay](./automaton_display.md) instance

## Example

```python title="render sample"
model = pytct.AutomatonDisplay("model")
model.render()
```

An image window will appear. If you are in a Jupyter environment, it will appear below the cell.

```python title="save sample"
model = pytct.AutomatonDisplay("model")
model.save("model")
```

The file is saved as "model.png" in the current directory.