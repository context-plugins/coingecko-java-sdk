
# Roi

Return on investment

*This model accepts additional fields of type Object.*

## Structure

`Roi`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Times` | [`Double`](../../doc/models/precision.md) | Optional | ROI multiplier | Double getTimes() | setTimes(Double times) |
| `Currency` | `String` | Optional | ROI currency | String getCurrency() | setCurrency(String currency) |
| `Percentage` | [`Double`](../../doc/models/precision.md) | Optional | ROI percentage | Double getPercentage() | setPercentage(Double percentage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Roi;
import java.io.IOException;

Roi roi = new Roi.Builder()
    .times(28.88D)
    .currency("currency0")
    .percentage(145.98D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

