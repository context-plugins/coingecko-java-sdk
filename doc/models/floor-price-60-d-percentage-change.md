
# Floor Price 60 D Percentage Change

NFT collection floor price 60 days percentage change

*This model accepts additional fields of type Object.*

## Structure

`FloorPrice60DPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.FloorPrice60DPercentageChange;
import java.io.IOException;

FloorPrice60DPercentageChange floorPrice60DPercentageChange = new FloorPrice60DPercentageChange.Builder()
    .usd(114.78D)
    .nativeCurrency(59.42D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

