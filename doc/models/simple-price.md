
# Simple Price

*This model accepts additional fields of type Object.*

## Structure

`SimplePrice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | Price in the target currency | Double getUsd() | setUsd(Double usd) |
| `UsdMarketCap` | [`Double`](../../doc/models/precision.md) | Optional | Market capitalization in the target currency | Double getUsdMarketCap() | setUsdMarketCap(Double usdMarketCap) |
| `Usd24HVol` | [`Double`](../../doc/models/precision.md) | Optional | 24-hour trading volume in the target currency | Double getUsd24HVol() | setUsd24HVol(Double usd24HVol) |
| `Usd24HChange` | [`Double`](../../doc/models/precision.md) | Optional | 24-hour price change percentage in the target currency | Double getUsd24HChange() | setUsd24HChange(Double usd24HChange) |
| `LastUpdatedAt` | [`Double`](../../doc/models/precision.md) | Optional | Last updated timestamp in UNIX seconds | Double getLastUpdatedAt() | setLastUpdatedAt(Double lastUpdatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.SimplePrice;
import java.io.IOException;

SimplePrice simplePrice = new SimplePrice.Builder()
    .usd(64.78D)
    .usdMarketCap(103.96D)
    .usd24HVol(36.12D)
    .usd24HChange(234.52D)
    .lastUpdatedAt(14.9D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

