
# Coins Id History

*This model accepts additional fields of type Object.*

## Structure

`CoinsIdHistory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `Localization` | `Map<String, String>` | Optional | Localized coin names keyed by locale code | Map<String, String> getLocalization() | setLocalization(Map<String, String> localization) |
| `Image` | [`Image`](../../doc/models/image.md) | Required | Coin image URLs | Image getImage() | setImage(Image image) |
| `MarketData` | [`MarketData`](../../doc/models/market-data.md) | Required | Market data at the given date | MarketData getMarketData() | setMarketData(MarketData marketData) |
| `CommunityData` | [`CommunityData`](../../doc/models/community-data.md) | Required | Community engagement data | CommunityData getCommunityData() | setCommunityData(CommunityData communityData) |
| `DeveloperData` | [`DeveloperData`](../../doc/models/developer-data.md) | Required | Developer activity data | DeveloperData getDeveloperData() | setDeveloperData(DeveloperData developerData) |
| `PublicInterestStats` | [`PublicInterestStats`](../../doc/models/public-interest-stats.md) | Required | Public interest statistics | PublicInterestStats getPublicInterestStats() | setPublicInterestStats(PublicInterestStats publicInterestStats) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CoinsIdHistory;
import com.coingecko.api.models.CommunityData;
import com.coingecko.api.models.DeveloperData;
import com.coingecko.api.models.Image;
import com.coingecko.api.models.MarketData;
import com.coingecko.api.models.PublicInterestStats;
import java.io.IOException;
import java.util.LinkedHashMap;

CoinsIdHistory coinsIdHistory = new CoinsIdHistory.Builder(
    "id6",
    "symbol2",
    "name6",
    new Image.Builder()
        .thumb("thumb4")
        .small("small0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new MarketData.Builder()
        .currentPrice(new LinkedHashMap<String, Double>() {{
            put("key0", 235.13D);
            put("key1", 235.14D);
        }})
        .marketCap(new LinkedHashMap<String, Double>() {{
            put("key0", 150.21D);
            put("key1", 150.2D);
            put("key2", 150.19D);
        }})
        .totalVolume(new LinkedHashMap<String, Double>() {{
            put("key0", 235.12D);
            put("key1", 235.13D);
        }})
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new CommunityData.Builder()
        .facebookLikes(230.38D)
        .redditAveragePosts48H(178.44D)
        .redditAverageComments48H(47.96D)
        .redditSubscribers(50.74D)
        .redditAccountsActive48H(153.56D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new DeveloperData.Builder()
        .forks(63.8D)
        .stars(132.7D)
        .subscribers(173.76D)
        .totalIssues(68.92D)
        .closedIssues(119.96D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new PublicInterestStats.Builder()
        .alexaRank(73.98D)
        .bingMatches(52.2D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
)
.localization(new LinkedHashMap<String, String>() {{
        put("key0", "localization8");
    }})
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

