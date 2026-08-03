
# Buy Volume Usd

Buy volume in USD over various timeframes

*This model accepts additional fields of type Object.*

## Structure

`BuyVolumeUsd`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `M5` | `String` | Optional | - | String getM5() | setM5(String m5) |
| `M15` | `String` | Optional | - | String getM15() | setM15(String m15) |
| `M30` | `String` | Optional | - | String getM30() | setM30(String m30) |
| `H1` | `String` | Optional | - | String getH1() | setH1(String h1) |
| `H6` | `String` | Optional | - | String getH6() | setH6(String h6) |
| `H24` | `String` | Optional | - | String getH24() | setH24(String h24) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.BuyVolumeUsd;
import java.io.IOException;

BuyVolumeUsd buyVolumeUsd = new BuyVolumeUsd.Builder()
    .m5("m54")
    .m15("m152")
    .m30("m300")
    .h1("h14")
    .h6("h66")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

