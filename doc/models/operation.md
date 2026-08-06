
# Operation

indicates what to do with the file: "create" for creating a new file, "update" for updating an existing file,
"upload" for creating or updating a file, "rename" for renaming a file, and "delete" for deleting an existing file.

## Enumeration

`Operation`

## Fields

| Name |
|  --- |
| `CREATE` |
| `UPDATE` |
| `UPLOAD` |
| `RENAME` |
| `DELETE` |

## Example

```python
from gitea.models.operation import Operation

operation = Operation.DELETE
```

