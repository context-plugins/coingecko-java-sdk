
# Volume Usd 1

Volume in USD

*This model accepts additional fields of type Object.*

## Structure

`VolumeUsd1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `H24` | `String` | Optional | - | String getH24() | setH24(String h24) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.VolumeUsd1;
import java.io.IOException;

VolumeUsd1 volumeUsd1 = new VolumeUsd1.Builder()
    .h24("h248")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

