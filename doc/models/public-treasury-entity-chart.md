
# Public Treasury Entity Chart

*This model accepts additional fields of type Object.*

## Structure

`PublicTreasuryEntityChart`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Holdings` | [`List<List<Double>>`](../../doc/models/precision.md) | Required | Historical holdings data as [timestamp, amount] pairs | List<List<Double>> getHoldings() | setHoldings(List<List<Double>> holdings) |
| `HoldingValueInUsd` | [`List<List<Double>>`](../../doc/models/precision.md) | Required | Historical holdings value in USD as [timestamp, value_usd] pairs | List<List<Double>> getHoldingValueInUsd() | setHoldingValueInUsd(List<List<Double>> holdingValueInUsd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.PublicTreasuryEntityChart;
import java.io.IOException;
import java.util.Arrays;

PublicTreasuryEntityChart publicTreasuryEntityChart = new PublicTreasuryEntityChart.Builder(
    Arrays.asList(
        Arrays.asList(
            123.94D
        )
    ),
    Arrays.asList(
        Arrays.asList(
            140.7D,
            140.69D,
            140.68D
        ),
        Arrays.asList(
            140.7D,
            140.69D,
            140.68D
        ),
        Arrays.asList(
            140.7D,
            140.69D,
            140.68D
        )
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

