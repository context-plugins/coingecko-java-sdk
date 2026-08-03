
# Ath Change Percentage

NFT collection all time highs change percentage

*This model accepts additional fields of type Object.*

## Structure

`AthChangePercentage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.AthChangePercentage;
import java.io.IOException;

AthChangePercentage athChangePercentage = new AthChangePercentage.Builder()
    .nativeCurrency(58.72D)
    .usd(115.48D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

