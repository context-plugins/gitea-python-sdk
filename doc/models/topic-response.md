
# Topic Response

TopicResponse for returning topics

*This model accepts additional fields of type Any.*

## Structure

`TopicResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `datetime` | Optional | The date and time when the topic was created |
| `id` | `int` | Optional | The unique identifier of the topic |
| `repo_count` | `int` | Optional | The number of repositories using this topic |
| `topic_name` | `str` | Optional | The name of the topic |
| `updated` | `datetime` | Optional | The date and time when the topic was last updated |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.topic_response import TopicResponse

topic_response = TopicResponse(
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=136,
    repo_count=166,
    topic_name='topic_name0',
    updated=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

