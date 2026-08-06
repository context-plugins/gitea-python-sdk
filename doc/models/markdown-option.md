
# Markdown Option

MarkdownOption markdown options

*This model accepts additional fields of type Any.*

## Structure

`MarkdownOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | `str` | Optional | URL path for rendering issue, media and file links<br>Expected format: /subpath/{user}/{repo}/src/{branch, commit, tag}/{identifier/path}/{file/dir} |
| `mode` | `str` | Optional | Mode to render (markdown, comment, wiki, file) |
| `text` | `str` | Optional | Text markdown to render |
| `wiki` | `bool` | Optional | Is it a wiki page? (use mode=wiki instead)<br><br>Deprecated: true |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.markdown_option import MarkdownOption

markdown_option = MarkdownOption(
    context='Context8',
    mode='Mode0',
    text='Text8',
    wiki=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

