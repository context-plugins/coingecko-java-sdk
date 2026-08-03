
# Community Data 1

Community data

*This model accepts additional fields of type Object.*

## Structure

`CommunityData1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FacebookLikes` | [`Double`](../../doc/models/precision.md) | Optional | Facebook likes | Double getFacebookLikes() | setFacebookLikes(Double facebookLikes) |
| `RedditAveragePosts48H` | [`Double`](../../doc/models/precision.md) | Optional | Reddit average posts in 48 hours | Double getRedditAveragePosts48H() | setRedditAveragePosts48H(Double redditAveragePosts48H) |
| `RedditAverageComments48H` | [`Double`](../../doc/models/precision.md) | Optional | Reddit average comments in 48 hours | Double getRedditAverageComments48H() | setRedditAverageComments48H(Double redditAverageComments48H) |
| `RedditSubscribers` | [`Double`](../../doc/models/precision.md) | Optional | Reddit subscribers | Double getRedditSubscribers() | setRedditSubscribers(Double redditSubscribers) |
| `RedditAccountsActive48H` | [`Double`](../../doc/models/precision.md) | Optional | Reddit active accounts in 48 hours | Double getRedditAccountsActive48H() | setRedditAccountsActive48H(Double redditAccountsActive48H) |
| `TelegramChannelUserCount` | [`Double`](../../doc/models/precision.md) | Optional | Telegram channel user count | Double getTelegramChannelUserCount() | setTelegramChannelUserCount(Double telegramChannelUserCount) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CommunityData1;
import java.io.IOException;

CommunityData1 communityData1 = new CommunityData1.Builder()
    .facebookLikes(221.52D)
    .redditAveragePosts48H(169.58D)
    .redditAverageComments48H(39.1D)
    .redditSubscribers(59.6D)
    .redditAccountsActive48H(93.58D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

