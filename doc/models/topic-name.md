
# Topic Name

TopicName a list of repo topic names

*This model accepts additional fields of type Any.*

## Structure

`TopicName`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `topics` | `List[str]` | Optional | List of topic names |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.topic_name import TopicName

topic_name = TopicName(
    topics=[
        'topics3',
        'topics4'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

