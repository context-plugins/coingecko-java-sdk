
# Market Data

Market data at the given date

*This model accepts additional fields of type Object.*

## Structure

`MarketData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CurrentPrice` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Current price keyed by currency | Map<String, Double> getCurrentPrice() | setCurrentPrice(Map<String, Double> currentPrice) |
| `MarketCap` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Market capitalization keyed by currency | Map<String, Double> getMarketCap() | setMarketCap(Map<String, Double> marketCap) |
| `TotalVolume` | [`Map<String, Double>`](../../doc/models/precision.md) | Optional | Total trading volume keyed by currency | Map<String, Double> getTotalVolume() | setTotalVolume(Map<String, Double> totalVolume) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.MarketData;
import java.io.IOException;
import java.util.LinkedHashMap;

MarketData marketData = new MarketData.Builder()
    .currentPrice(new LinkedHashMap<String, Double>() {{
        put("key0", 155.85D);
        put("key1", 155.86D);
    }})
    .marketCap(new LinkedHashMap<String, Double>() {{
        put("key0", 57.59D);
        put("key1", 57.6D);
    }})
    .totalVolume(new LinkedHashMap<String, Double>() {{
        put("key0", 155.84D);
        put("key1", 155.85D);
    }})
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

