
# Developer Data

Developer activity data

*This model accepts additional fields of type Object.*

## Structure

`DeveloperData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Forks` | [`Double`](../../doc/models/precision.md) | Optional | Repository forks | Double getForks() | setForks(Double forks) |
| `Stars` | [`Double`](../../doc/models/precision.md) | Optional | Repository stars | Double getStars() | setStars(Double stars) |
| `Subscribers` | [`Double`](../../doc/models/precision.md) | Optional | Repository subscribers | Double getSubscribers() | setSubscribers(Double subscribers) |
| `TotalIssues` | [`Double`](../../doc/models/precision.md) | Optional | Total issues | Double getTotalIssues() | setTotalIssues(Double totalIssues) |
| `ClosedIssues` | [`Double`](../../doc/models/precision.md) | Optional | Closed issues | Double getClosedIssues() | setClosedIssues(Double closedIssues) |
| `PullRequestsMerged` | [`Double`](../../doc/models/precision.md) | Optional | Pull requests merged | Double getPullRequestsMerged() | setPullRequestsMerged(Double pullRequestsMerged) |
| `PullRequestContributors` | [`Double`](../../doc/models/precision.md) | Optional | Pull request contributors | Double getPullRequestContributors() | setPullRequestContributors(Double pullRequestContributors) |
| `CodeAdditionsDeletions4Weeks` | [`CodeAdditionsDeletions4Weeks`](../../doc/models/code-additions-deletions-4-weeks.md) | Optional | Code additions and deletions in the last 4 weeks | CodeAdditionsDeletions4Weeks getCodeAdditionsDeletions4Weeks() | setCodeAdditionsDeletions4Weeks(CodeAdditionsDeletions4Weeks codeAdditionsDeletions4Weeks) |
| `CommitCount4Weeks` | [`Double`](../../doc/models/precision.md) | Optional | Commit count in the last 4 weeks | Double getCommitCount4Weeks() | setCommitCount4Weeks(Double commitCount4Weeks) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DeveloperData;
import java.io.IOException;

DeveloperData developerData = new DeveloperData.Builder()
    .forks(3.36D)
    .stars(199.86D)
    .subscribers(240.92D)
    .totalIssues(136.08D)
    .closedIssues(187.12D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

