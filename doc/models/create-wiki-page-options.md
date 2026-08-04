
# Create Wiki Page Options

CreateWikiPageOptions form for creating wiki

*This model accepts additional fields of type Any.*

## Structure

`CreateWikiPageOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content_base_64` | `str` | Optional | content must be base64 encoded |
| `message` | `str` | Optional | optional commit message summarizing the change |
| `title` | `str` | Optional | page title. leave empty to keep unchanged |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_wiki_page_options import CreateWikiPageOptions

create_wiki_page_options = CreateWikiPageOptions(
    content_base_64='content_base648',
    message='message8',
    title='title2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

