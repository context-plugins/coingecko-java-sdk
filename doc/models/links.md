
# Links

Links

*This model accepts additional fields of type Object.*

## Structure

`Links`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Homepage` | `List<String>` | Optional | Website URL | List<String> getHomepage() | setHomepage(List<String> homepage) |
| `Whitepaper` | `String` | Optional | Whitepaper URL | String getWhitepaper() | setWhitepaper(String whitepaper) |
| `BlockchainSite` | `List<String>` | Optional | Block explorer URL | List<String> getBlockchainSite() | setBlockchainSite(List<String> blockchainSite) |
| `OfficialForumUrl` | `List<String>` | Optional | Official forum URL | List<String> getOfficialForumUrl() | setOfficialForumUrl(List<String> officialForumUrl) |
| `ChatUrl` | `List<String>` | Optional | Chat URL | List<String> getChatUrl() | setChatUrl(List<String> chatUrl) |
| `AnnouncementUrl` | `List<String>` | Optional | Announcement URL | List<String> getAnnouncementUrl() | setAnnouncementUrl(List<String> announcementUrl) |
| `SnapshotUrl` | `String` | Optional | Snapshot URL | String getSnapshotUrl() | setSnapshotUrl(String snapshotUrl) |
| `TwitterScreenName` | `String` | Optional | Twitter handle | String getTwitterScreenName() | setTwitterScreenName(String twitterScreenName) |
| `FacebookUsername` | `String` | Optional | Facebook username | String getFacebookUsername() | setFacebookUsername(String facebookUsername) |
| `BitcointalkThreadIdentifier` | `Integer` | Optional | Bitcointalk thread identifier | Integer getBitcointalkThreadIdentifier() | setBitcointalkThreadIdentifier(Integer bitcointalkThreadIdentifier) |
| `TelegramChannelIdentifier` | `String` | Optional | Telegram channel identifier | String getTelegramChannelIdentifier() | setTelegramChannelIdentifier(String telegramChannelIdentifier) |
| `SubredditUrl` | `String` | Optional | Subreddit URL | String getSubredditUrl() | setSubredditUrl(String subredditUrl) |
| `ReposUrl` | [`ReposUrl`](../../doc/models/repos-url.md) | Optional | Repository URL | ReposUrl getReposUrl() | setReposUrl(ReposUrl reposUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Links;
import java.io.IOException;
import java.util.Arrays;

Links links = new Links.Builder()
    .homepage(Arrays.asList(
        "homepage8",
        "homepage9",
        "homepage0"
    ))
    .whitepaper("whitepaper2")
    .blockchainSite(Arrays.asList(
        "blockchain_site1",
        "blockchain_site2",
        "blockchain_site3"
    ))
    .officialForumUrl(Arrays.asList(
        "official_forum_url8",
        "official_forum_url9"
    ))
    .chatUrl(Arrays.asList(
        "chat_url2"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

