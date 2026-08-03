
# Floor Price 14 D Percentage Change

NFT collection floor price 14 days percentage change

*This model accepts additional fields of type Object.*

## Structure

`FloorPrice14DPercentageChange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `NativeCurrency` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getNativeCurrency() | setNativeCurrency(Double nativeCurrency) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.FloorPrice14DPercentageChange;
import java.io.IOException;

FloorPrice14DPercentageChange floorPrice14DPercentageChange = new FloorPrice14DPercentageChange.Builder()
    .usd(13.44D)
    .nativeCurrency(187.64D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

