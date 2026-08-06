
# User Badge Option

UserBadgeOption options for link between users and badges

*This model accepts additional fields of type Any.*

## Structure

`UserBadgeOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `badge_slugs` | `List[str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.user_badge_option import UserBadgeOption

user_badge_option = UserBadgeOption(
    badge_slugs=[
        'badge1',
        'badge2'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

