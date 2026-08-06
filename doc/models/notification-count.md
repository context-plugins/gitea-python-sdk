
# Notification Count

NotificationCount number of unread notifications

*This model accepts additional fields of type Any.*

## Structure

`NotificationCount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `new` | `int` | Optional | New is the number of unread notifications |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.notification_count import NotificationCount

notification_count = NotificationCount(
    new=106,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

