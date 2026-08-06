
# Package

Package represents a package

*This model accepts additional fields of type Any.*

## Structure

`Package`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | - |
| `creator` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `html_url` | `str` | Optional | The HTML URL to view the package |
| `id` | `int` | Optional | The unique identifier of the package |
| `name` | `str` | Optional | The name of the package |
| `owner` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `repository` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `mtype` | `str` | Optional | The type of the package (e.g., npm, maven, docker) |
| `version` | `str` | Optional | The version of the package |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.package import Package
from gitea.models.user import User

package = Package(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    creator=User(
        active=False,
        avatar_url='avatar_url4',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description2',
        email='email8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    html_url='html_url2',
    id=146,
    name='name8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

