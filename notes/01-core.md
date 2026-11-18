# Deduplicate while preserving order: implementation

## What the example does

Dictionary keys preserve insertion order. This recipe accepts hashable JSON scalars; nested lists or objects are not valid keys.

The public function is `solve(value)`. The JSON input contract can be seen in this concrete example:

```json
[
  "b",
  "a",
  "b",
  "c"
]
```

Expected result:

```json
[
  "b",
  "a",
  "c"
]
```

Run `python3 example.py` for the Python representation of the result. `solution.py` contains the full implementation and can also be imported by another script.

## Scope

The function implements exactly the behavior described above. It does not perform network or filesystem access. Python exceptions indicate unsupported input; the next lesson turns them into a command-line error response. Review the limitations before reusing it in an application.
