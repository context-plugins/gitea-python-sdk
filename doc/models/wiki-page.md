
# Wiki Page

WikiPage a wiki page

*This model accepts additional fields of type Any.*

## Structure

`WikiPage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commit_count` | `int` | Optional | The number of commits that modified this page |
| `content_base_64` | `str` | Optional | Page content, base64 encoded |
| `footer` | `str` | Optional | The footer content for the wiki page |
| `html_url` | `str` | Optional | The HTML URL to view the wiki page |
| `last_commit` | [`WikiCommit`](../../doc/models/wiki-commit.md) | Optional | WikiCommit page commit/revision |
| `sidebar` | `str` | Optional | The sidebar content for the wiki page |
| `sub_url` | `str` | Optional | The sub URL path for the wiki page |
| `title` | `str` | Optional | The title of the wiki page |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.commit_user_contains_information_of_a_user_in_the_context_of_a_commit import CommitUserContainsInformationOfAUserInTheContextOfACommit
from gitea.models.wiki_commit import WikiCommit
from gitea.models.wiki_page import WikiPage

wiki_page = WikiPage(
    commit_count=240,
    content_base_64='content_base644',
    footer='footer0',
    html_url='html_url2',
    last_commit=WikiCommit(
        author=CommitUserContainsInformationOfAUserInTheContextOfACommit(
            date='date6',
            email='email6',
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        commiter=CommitUserContainsInformationOfAUserInTheContextOfACommit(
            date='date2',
            email='email4',
            name='name2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        message='message8',
        sha='sha4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

