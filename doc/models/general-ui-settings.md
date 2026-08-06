
# General Ui Settings

GeneralUISettings contains global ui settings exposed by API

*This model accepts additional fields of type Any.*

## Structure

`GeneralUiSettings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allowed_reactions` | `List[str]` | Optional | AllowedReactions contains the list of allowed emoji reactions |
| `custom_emojis` | `List[str]` | Optional | CustomEmojis contains the list of custom emojis |
| `default_theme` | `str` | Optional | DefaultTheme is the default UI theme |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.general_ui_settings import GeneralUiSettings

general_ui_settings = GeneralUiSettings(
    allowed_reactions=[
        'allowed_reactions9',
        'allowed_reactions0',
        'allowed_reactions1'
    ],
    custom_emojis=[
        'custom_emojis3',
        'custom_emojis4'
    ],
    default_theme='default_theme6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

