
# Floor Price 24 H Percentage Change

NFT collection floor price 24 hours percentage change

*This model accepts additional fields of type Object.*

## Structure

`FloorPrice24HPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.FloorPrice24HPercentageChange;
import java.io.IOException;

FloorPrice24HPercentageChange floorPrice24HPercentageChange = new FloorPrice24HPercentageChange.Builder()
    .usd(162.94D)
    .nativeCurrency(81.14D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

