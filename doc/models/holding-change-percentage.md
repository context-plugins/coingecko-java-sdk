
# Holding Change Percentage

Holding change percentages over different timeframes

*This model accepts additional fields of type Object.*

## Structure

`HoldingChangePercentage`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `M7D` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getM7D() | setM7D(Double m7D) |
| `M14D` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getM14D() | setM14D(Double m14D) |
| `M30D` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getM30D() | setM30D(Double m30D) |
| `M90D` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getM90D() | setM90D(Double m90D) |
| `M1Y` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getM1Y() | setM1Y(Double m1Y) |
| `Ytd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getYtd() | setYtd(Double ytd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.HoldingChangePercentage;
import java.io.IOException;

HoldingChangePercentage holdingChangePercentage = new HoldingChangePercentage.Builder()
    .m7D(54.1D)
    .m14D(115.62D)
    .m30D(77.84D)
    .m90D(14.9D)
    .m1Y(59.96D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

