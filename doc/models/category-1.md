
# Category 1

*This model accepts additional fields of type Object.*

## Structure

`Category1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Category ID | String getId() | setId(String id) |
| `Name` | `String` | Required | Category name | String getName() | setName(String name) |
| `MarketCap` | [`double`](../../doc/models/precision.md) | Required | Category market cap | double getMarketCap() | setMarketCap(double marketCap) |
| `MarketCapChange24H` | [`double`](../../doc/models/precision.md) | Required | Category market cap change in 24 hours | double getMarketCapChange24H() | setMarketCapChange24H(double marketCapChange24H) |
| `Content` | `String` | Required | Category description | String getContent() | setContent(String content) |
| `Top3CoinsId` | `List<String>` | Required | IDs of top 3 coins in the category | List<String> getTop3CoinsId() | setTop3CoinsId(List<String> top3CoinsId) |
| `Top3Coins` | `List<String>` | Required | Image URLs of top 3 coins in the category | List<String> getTop3Coins() | setTop3Coins(List<String> top3Coins) |
| `Volume24H` | [`double`](../../doc/models/precision.md) | Required | Category trading volume in 24 hours | double getVolume24H() | setVolume24H(double volume24H) |
| `UpdatedAt` | `String` | Required | Category last updated timestamp | String getUpdatedAt() | setUpdatedAt(String updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Category1;
import java.io.IOException;
import java.util.Arrays;

Category1 category1 = new Category1.Builder(
    "id0",
    "name0",
    53.1D,
    136.34D,
    "content4",
    Arrays.asList(
        "top_3_coins_id2",
        "top_3_coins_id3"
    ),
    Arrays.asList(
        "top_3_coins9"
    ),
    213.58D,
    "updated_at4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

