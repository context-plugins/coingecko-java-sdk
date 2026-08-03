
# Attributes 4

*This model accepts additional fields of type Object.*

## Structure

`Attributes4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OhlcvList` | [`List<List<Double>>`](../../doc/models/precision.md) | Required | OHLCV data as [timestamp, open, high, low, close, volume] arrays | List<List<Double>> getOhlcvList() | setOhlcvList(List<List<Double>> ohlcvList) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes4;
import java.io.IOException;
import java.util.Arrays;

Attributes4 attributes4 = new Attributes4.Builder(
    Arrays.asList(
        Arrays.asList(
            42.08D,
            42.09D,
            42.1D
        ),
        Arrays.asList(
            42.08D,
            42.09D,
            42.1D
        ),
        Arrays.asList(
            42.08D,
            42.09D,
            42.1D
        )
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

