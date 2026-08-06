
# Branch

Branch represents a repository branch

*This model accepts additional fields of type Any.*

## Structure

`Branch`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commit` | [`PayloadCommit`](../../doc/models/payload-commit.md) | Optional | PayloadCommit represents a commit |
| `effective_branch_protection_name` | `str` | Optional | EffectiveBranchProtectionName is the name of the effective branch protection rule |
| `enable_status_check` | `bool` | Optional | EnableStatusCheck indicates if status checks are enabled |
| `name` | `str` | Optional | Name is the branch name |
| `protected` | `bool` | Optional | Protected indicates if the branch is protected |
| `required_approvals` | `int` | Optional | RequiredApprovals is the number of required approvals for pull requests |
| `status_check_contexts` | `List[str]` | Optional | StatusCheckContexts contains the list of required status check contexts |
| `user_can_merge` | `bool` | Optional | UserCanMerge indicates if the current user can merge to this branch |
| `user_can_push` | `bool` | Optional | UserCanPush indicates if the current user can push to this branch |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.branch import Branch
from gitea.models.payload_commit import PayloadCommit
from gitea.models.payload_user import PayloadUser

branch = Branch(
    commit=PayloadCommit(
        added=[
            'added6',
            'added7'
        ],
        author=PayloadUser(
            email='email6',
            name='name0',
            username='username0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        committer=PayloadUser(
            email='email2',
            name='name4',
            username='username6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        id='id8',
        message='message2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    effective_branch_protection_name='effective_branch_protection_name0',
    enable_status_check=False,
    name='name6',
    protected=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

