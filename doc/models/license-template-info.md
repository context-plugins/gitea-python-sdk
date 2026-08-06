
# License Template Info

LicensesInfo contains information about a License

*This model accepts additional fields of type Any.*

## Structure

`LicenseTemplateInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | Body contains the full text of the license |
| `implementation` | `str` | Optional | Implementation contains license implementation details |
| `key` | `str` | Optional | Key is the unique identifier for the license template |
| `name` | `str` | Optional | Name is the display name of the license |
| `url` | `str` | Optional | URL is the reference URL for the license |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.license_template_info import LicenseTemplateInfo

license_template_info = LicenseTemplateInfo(
    body='body2',
    implementation='implementation8',
    key='key6',
    name='name6',
    url='url0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

