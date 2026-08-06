
# Markup Option

MarkupOption markup options

*This model accepts additional fields of type Any.*

## Structure

`MarkupOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | `str` | Optional | URL path for rendering issue, media and file links<br>Expected format: /subpath/{user}/{repo}/src/{branch, commit, tag}/{identifier/path}/{file/dir} |
| `file_path` | `str` | Optional | File path for detecting extension in file mode |
| `mode` | `str` | Optional | Mode to render (markdown, comment, wiki, file) |
| `text` | `str` | Optional | Text markup to render |
| `wiki` | `bool` | Optional | Is it a wiki page? (use mode=wiki instead)<br><br>Deprecated: true |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.markup_option import MarkupOption

markup_option = MarkupOption(
    context='Context8',
    file_path='FilePath2',
    mode='Mode0',
    text='Text8',
    wiki=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

