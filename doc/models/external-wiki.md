
# External Wiki

ExternalWiki represents setting for external wiki

*This model accepts additional fields of type Any.*

## Structure

`ExternalWiki`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_wiki_url` | `str` | Optional | URL of external wiki. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.external_wiki import ExternalWiki

external_wiki = ExternalWiki(
    external_wiki_url='external_wiki_url0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

