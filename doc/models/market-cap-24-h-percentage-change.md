
# Market Cap 24 H Percentage Change

NFT collection market cap 24 hours percentage change

*This model accepts additional fields of type Object.*

## Structure

`MarketCap24HPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.MarketCap24HPercentageChange;
import java.io.IOException;

MarketCap24HPercentageChange marketCap24HPercentageChange = new MarketCap24HPercentageChange.Builder()
    .usd(97.68D)
    .nativeCurrency(15.88D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

