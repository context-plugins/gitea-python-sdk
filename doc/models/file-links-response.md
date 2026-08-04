
# File Links Response

FileLinksResponse contains the links for a repo's file

*This model accepts additional fields of type Any.*

## Structure

`FileLinksResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `git` | `str` | Optional | GitURL is the Git API URL for this file |
| `html` | `str` | Optional | HTMLURL is the web URL for this file |
| `mself` | `str` | Optional | Self is the API URL for this file |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.file_links_response import FileLinksResponse

file_links_response = FileLinksResponse(
    git='git0',
    html='html2',
    mself='self0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

