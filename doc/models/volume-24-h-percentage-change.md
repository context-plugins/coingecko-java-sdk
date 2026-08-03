
# Volume 24 H Percentage Change

NFT collection volume in 24 hours percentage change

*This model accepts additional fields of type Object.*

## Structure

`Volume24HPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Volume24HPercentageChange;
import java.io.IOException;

Volume24HPercentageChange volume24HPercentageChange = new Volume24HPercentageChange.Builder()
    .usd(130.56D)
    .nativeCurrency(48.76D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

