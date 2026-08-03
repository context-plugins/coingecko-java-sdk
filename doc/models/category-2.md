
# Category 2

*This model accepts additional fields of type Object.*

## Structure

`Category2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | Category ID | int getId() | setId(int id) |
| `Name` | `String` | Required | Category name | String getName() | setName(String name) |
| `Top3CoinsImages` | `List<String>` | Required | Top 3 coins image URLs in the category | List<String> getTop3CoinsImages() | setTop3CoinsImages(List<String> top3CoinsImages) |
| `MarketCap1HChange` | [`double`](../../doc/models/precision.md) | Required | Category market cap 1 hour change | double getMarketCap1HChange() | setMarketCap1HChange(double marketCap1HChange) |
| `Slug` | `String` | Required | Category web slug | String getSlug() | setSlug(String slug) |
| `CoinsCount` | `String` | Required | Number of coins in the category | String getCoinsCount() | setCoinsCount(String coinsCount) |
| `Data` | [`Data4`](../../doc/models/data-4.md) | Required | - | Data4 getData() | setData(Data4 data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Category2;
import com.coingecko.api.models.Data4;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

Category2 category2 = new Category2.Builder(
    80,
    "name2",
    Arrays.asList(
        "top_3_coins_images4",
        "top_3_coins_images5"
    ),
    8.98D,
    "slug4",
    "coins_count6",
    new Data4.Builder(
        184.2D,
        21.84D,
        14.42D,
        197.04D,
        new LinkedHashMap<String, Double>() {{
            put("key0", 226.93D);
            put("key1", 226.94D);
            put("key2", 226.95D);
        }},
        "sparkline8"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

