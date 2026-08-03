
# Holding Amount Change

Holding amount changes over different timeframes

*This model accepts additional fields of type Object.*

## Structure

`HoldingAmountChange`

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
import com.coingecko.api.models.HoldingAmountChange;
import java.io.IOException;

HoldingAmountChange holdingAmountChange = new HoldingAmountChange.Builder()
    .m7D(194.58D)
    .m14D(0.1D)
    .m30D(37.68D)
    .m90D(130.42D)
    .m1Y(55.56D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

