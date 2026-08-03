
# Volume 24 H

NFT collection volume in 24 hours

*This model accepts additional fields of type Object.*

## Structure

`Volume24H`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Volume24H;
import java.io.IOException;

Volume24H volume24H = new Volume24H.Builder()
    .nativeCurrency(79.68D)
    .usd(161.48D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

