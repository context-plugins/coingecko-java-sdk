
# Data 2

*This model accepts additional fields of type Object.*

## Structure

`Data2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Price` | [`double`](../../doc/models/precision.md) | Required | Coin price in USD | double getPrice() | setPrice(double price) |
| `PriceBtc` | `String` | Required | Coin price in BTC | String getPriceBtc() | setPriceBtc(String priceBtc) |
| `PriceChangePercentage24H` | [`Map<String, Double>`](../../doc/models/precision.md) | Required | Coin price change percentage in 24 hours by currency | Map<String, Double> getPriceChangePercentage24H() | setPriceChangePercentage24H(Map<String, Double> priceChangePercentage24H) |
| `MarketCap` | `String` | Required | Coin market cap in USD | String getMarketCap() | setMarketCap(String marketCap) |
| `MarketCapBtc` | `String` | Required | Coin market cap in BTC | String getMarketCapBtc() | setMarketCapBtc(String marketCapBtc) |
| `TotalVolume` | `String` | Required | Coin total volume in USD | String getTotalVolume() | setTotalVolume(String totalVolume) |
| `TotalVolumeBtc` | `String` | Required | Coin total volume in BTC | String getTotalVolumeBtc() | setTotalVolumeBtc(String totalVolumeBtc) |
| `Sparkline` | `String` | Required | Coin sparkline image URL | String getSparkline() | setSparkline(String sparkline) |
| `Content` | [`Content`](../../doc/models/content.md) | Required | - | Content getContent() | setContent(Content content) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Content;
import com.coingecko.api.models.Data2;
import java.io.IOException;
import java.util.LinkedHashMap;

Data2 data2 = new Data2.Builder(
    43.38D,
    "price_btc2",
    new LinkedHashMap<String, Double>() {{
        put("key0", 242.91D);
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
.build();
```

