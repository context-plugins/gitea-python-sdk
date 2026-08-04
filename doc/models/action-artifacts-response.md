
# Action Artifacts Response

ActionArtifactsResponse returns ActionArtifacts

*This model accepts additional fields of type Any.*

## Structure

`ActionArtifactsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artifacts` | [`List[ActionArtifact]`](../../doc/models/action-artifact.md) | Optional | - |
| `total_count` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.action_artifact import ActionArtifact
from giteaapi.models.action_artifacts_response import ActionArtifactsResponse

action_artifacts_response = ActionArtifactsResponse(
    artifacts=[
        ActionArtifact(
            archive_download_url='archive_download_url0',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            expired=False,
            expires_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            id=168,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionArtifact(
            archive_download_url='archive_download_url0',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            expired=False,
            expires_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            id=168,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    total_count=12,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

