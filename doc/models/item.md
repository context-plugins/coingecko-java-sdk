
# Item

*This model accepts additional fields of type Object.*

## Structure

`Item`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `CoinId` | `int` | Required | Coin internal ID | int getCoinId() | setCoinId(int coinId) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `MarketCapRank` | `int` | Required | Coin market cap rank | int getMarketCapRank() | setMarketCapRank(int marketCapRank) |
| `Thumb` | `String` | Required | Coin thumb image URL | String getThumb() | setThumb(String thumb) |
| `Small` | `String` | Required | Coin small image URL | String getSmall() | setSmall(String small) |
| `Large` | `String` | Required | Coin large image URL | String getLarge() | setLarge(String large) |
| `Slug` | `String` | Required | Coin web slug | String getSlug() | setSlug(String slug) |
| `PriceBtc` | [`double`](../../doc/models/precision.md) | Required | Coin price in BTC | double getPriceBtc() | setPriceBtc(double priceBtc) |
| `Score` | `int` | Required | Coin trending rank (0-based) | int getScore() | setScore(int score) |
| `Data` | [`Data2`](../../doc/models/data-2.md) | Required | - | Data2 getData() | setData(Data2 data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Content;
import com.coingecko.api.models.Data2;
import com.coingecko.api.models.Item;
import java.io.IOException;
import java.util.LinkedHashMap;

Item item = new Item.Builder(
    "id2",
    118,
    "name2",
    "symbol4",
    162,
    "thumb0",
    "small6",
    "large4",
    "slug6",
    212.04D,
    28,
    new Data2.Builder(
        148.58D,
        "price_btc2",
        new LinkedHashMap<String, Double>() {{
            put("key0", 92.11D);
            put("key1", 92.12D);
            put("key2", 92.13D);
        }},
        "market_cap0",
        "market_cap_btc4",
        "total_volume2",
        "total_volume_btc4",
        "sparkline8",
        new Content.Builder()
            .title("title0")
            .description("description6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

