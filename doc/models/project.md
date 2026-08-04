
# Project

Project represents a project

*This model accepts additional fields of type Any.*

## Structure

`Project`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `closed_at` | `datetime` | Optional | - |
| `created_at` | `datetime` | Optional | - |
| `creator_id` | `int` | Optional | CreatorID is the user who created the project |
| `description` | `str` | Optional | Description provides details about the project |
| `id` | `int` | Optional | ID is the unique identifier for the project |
| `is_closed` | `bool` | Optional | IsClosed indicates if the project is closed |
| `owner_id` | `int` | Optional | OwnerID is the owner of the project (for org-level projects) |
| `repo_id` | `int` | Optional | RepoID is the repository this project belongs to (for repo-level projects) |
| `title` | `str` | Optional | Title is the title of the project |
| `updated_at` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.project import Project

project = Project(
    closed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    creator_id=226,
    description='description4',
    id=228,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

