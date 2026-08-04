
# Licenses Template List Entry

LicensesListEntry is used for the API

*This model accepts additional fields of type Any.*

## Structure

`LicensesTemplateListEntry`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `str` | Optional | Key is the unique identifier for the license template |
| `name` | `str` | Optional | Name is the display name of the license |
| `url` | `str` | Optional | URL is the reference URL for the license |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.licenses_template_list_entry import LicensesTemplateListEntry

licenses_template_list_entry = LicensesTemplateListEntry(
    key='key2',
    name='name2',
    url='url6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

