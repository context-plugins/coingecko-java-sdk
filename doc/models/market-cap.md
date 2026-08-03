
# Market Cap

NFT collection market cap

*This model accepts additional fields of type Object.*

## Structure

`MarketCap`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.MarketCap;
import java.io.IOException;

MarketCap marketCap = new MarketCap.Builder()
    .nativeCurrency(247.56D)
    .usd(73.36D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

