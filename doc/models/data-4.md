
# Data 4

*This model accepts additional fields of type Object.*

## Structure

`Data4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MarketCap` | [`double`](../../doc/models/precision.md) | Required | Category market cap | double getMarketCap() | setMarketCap(double marketCap) |
| `MarketCapBtc` | [`double`](../../doc/models/precision.md) | Required | Category market cap in BTC | double getMarketCapBtc() | setMarketCapBtc(double marketCapBtc) |
| `TotalVolume` | [`double`](../../doc/models/precision.md) | Required | Category total volume | double getTotalVolume() | setTotalVolume(double totalVolume) |
| `TotalVolumeBtc` | [`double`](../../doc/models/precision.md) | Required | Category total volume in BTC | double getTotalVolumeBtc() | setTotalVolumeBtc(double totalVolumeBtc) |
| `MarketCapChangePercentage24H` | [`Map<String, Double>`](../../doc/models/precision.md) | Required | Category market cap change percentage in 24 hours by currency | Map<String, Double> getMarketCapChangePercentage24H() | setMarketCapChangePercentage24H(Map<String, Double> marketCapChangePercentage24H) |
| `Sparkline` | `String` | Required | Category sparkline image URL | String getSparkline() | setSparkline(String sparkline) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data4;
import java.io.IOException;
import java.util.LinkedHashMap;

Data4 data4 = new Data4.Builder(
    0.64D,
    93D,
    85.58D,
    243.8D,
    new LinkedHashMap<String, Double>() {{
        put("key0", 42.09D);
    }},
    "sparkline4"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

