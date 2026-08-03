
# Floor Price 30 D Percentage Change

NFT collection floor price 30 days percentage change

*This model accepts additional fields of type Object.*

## Structure

`FloorPrice30DPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.FloorPrice30DPercentageChange;
import java.io.IOException;

FloorPrice30DPercentageChange floorPrice30DPercentageChange = new FloorPrice30DPercentageChange.Builder()
    .usd(110.32D)
    .nativeCurrency(28.52D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

