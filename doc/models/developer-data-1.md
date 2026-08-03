
# Developer Data 1

Developer data

*This model accepts additional fields of type Object.*

## Structure

`DeveloperData1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Forks` | [`Double`](../../doc/models/precision.md) | Optional | Repository forks | Double getForks() | setForks(Double forks) |
| `Stars` | [`Double`](../../doc/models/precision.md) | Optional | Repository stars | Double getStars() | setStars(Double stars) |
| `Subscribers` | [`Double`](../../doc/models/precision.md) | Optional | Repository subscribers | Double getSubscribers() | setSubscribers(Double subscribers) |
| `TotalIssues` | [`Double`](../../doc/models/precision.md) | Optional | Repository total issues | Double getTotalIssues() | setTotalIssues(Double totalIssues) |
| `ClosedIssues` | [`Double`](../../doc/models/precision.md) | Optional | Repository closed issues | Double getClosedIssues() | setClosedIssues(Double closedIssues) |
| `PullRequestsMerged` | [`Double`](../../doc/models/precision.md) | Optional | Repository pull requests merged | Double getPullRequestsMerged() | setPullRequestsMerged(Double pullRequestsMerged) |
| `PullRequestContributors` | [`Double`](../../doc/models/precision.md) | Optional | Repository pull request contributors | Double getPullRequestContributors() | setPullRequestContributors(Double pullRequestContributors) |
| `CodeAdditionsDeletions4Weeks` | [`CodeAdditionsDeletions4Weeks1`](../../doc/models/code-additions-deletions-4-weeks-1.md) | Optional | Code additions and deletions in 4 weeks | CodeAdditionsDeletions4Weeks1 getCodeAdditionsDeletions4Weeks() | setCodeAdditionsDeletions4Weeks(CodeAdditionsDeletions4Weeks1 codeAdditionsDeletions4Weeks) |
| `CommitCount4Weeks` | [`Double`](../../doc/models/precision.md) | Optional | Repository commit count in 4 weeks | Double getCommitCount4Weeks() | setCommitCount4Weeks(Double commitCount4Weeks) |
| `Last4WeeksCommitActivitySeries` | [`List<Double>`](../../doc/models/precision.md) | Optional | Repository last 4 weeks commit activity series | List<Double> getLast4WeeksCommitActivitySeries() | setLast4WeeksCommitActivitySeries(List<Double> last4WeeksCommitActivitySeries) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DeveloperData1;
import java.io.IOException;

DeveloperData1 developerData1 = new DeveloperData1.Builder()
    .forks(43.76D)
    .stars(152.74D)
    .subscribers(193.8D)
    .totalIssues(88.96D)
    .closedIssues(140D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

