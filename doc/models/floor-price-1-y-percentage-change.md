
# Floor Price 1 Y Percentage Change

NFT collection floor price 1 year percentage change

*This model accepts additional fields of type Object.*

## Structure

`FloorPrice1YPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.FloorPrice1YPercentageChange;
import java.io.IOException;

FloorPrice1YPercentageChange floorPrice1YPercentageChange = new FloorPrice1YPercentageChange.Builder()
    .usd(16.02D)
    .nativeCurrency(190.22D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

