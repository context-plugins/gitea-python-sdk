
# Repo Topic Options

RepoTopicOptions a collection of repo topic names

*This model accepts additional fields of type Any.*

## Structure

`RepoTopicOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `topics` | `List[str]` | Optional | list of topic names |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.repo_topic_options import RepoTopicOptions

repo_topic_options = RepoTopicOptions(
    topics=[
        'topics9',
        'topics0'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

