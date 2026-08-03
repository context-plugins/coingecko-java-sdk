
# Community Data

Community engagement data

*This model accepts additional fields of type Object.*

## Structure

`CommunityData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FacebookLikes` | [`Double`](../../doc/models/precision.md) | Optional | Number of Facebook likes | Double getFacebookLikes() | setFacebookLikes(Double facebookLikes) |
| `RedditAveragePosts48H` | [`Double`](../../doc/models/precision.md) | Optional | Average Reddit posts in 48 hours | Double getRedditAveragePosts48H() | setRedditAveragePosts48H(Double redditAveragePosts48H) |
| `RedditAverageComments48H` | [`Double`](../../doc/models/precision.md) | Optional | Average Reddit comments in 48 hours | Double getRedditAverageComments48H() | setRedditAverageComments48H(Double redditAverageComments48H) |
| `RedditSubscribers` | [`Double`](../../doc/models/precision.md) | Optional | Number of Reddit subscribers | Double getRedditSubscribers() | setRedditSubscribers(Double redditSubscribers) |
| `RedditAccountsActive48H` | [`Double`](../../doc/models/precision.md) | Optional | Active Reddit accounts in 48 hours | Double getRedditAccountsActive48H() | setRedditAccountsActive48H(Double redditAccountsActive48H) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CommunityData;
import java.io.IOException;

CommunityData communityData = new CommunityData.Builder()
    .facebookLikes(31.48D)
    .redditAveragePosts48H(235.54D)
    .redditAverageComments48H(150.94D)
    .redditSubscribers(249.64D)
    .redditAccountsActive48H(96.46D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

