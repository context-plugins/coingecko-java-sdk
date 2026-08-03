
# Floor Price 7 D Percentage Change

NFT collection floor price 7 days percentage change

*This model accepts additional fields of type Object.*

## Structure

`FloorPrice7DPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.FloorPrice7DPercentageChange;
import java.io.IOException;

FloorPrice7DPercentageChange floorPrice7DPercentageChange = new FloorPrice7DPercentageChange.Builder()
    .usd(214.64D)
    .nativeCurrency(132.84D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

