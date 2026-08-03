
# Sparkline in 7 D

Sparkline price data for the last 7 days

*This model accepts additional fields of type Object.*

## Structure

`SparklineIn7D`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Price` | [`List<Double>`](../../doc/models/precision.md) | Optional | Array of price values | List<Double> getPrice() | setPrice(List<Double> price) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.SparklineIn7D;
import java.io.IOException;
import java.util.Arrays;

SparklineIn7D sparklineIn7D = new SparklineIn7D.Builder()
    .price(Arrays.asList(
        30.38D,
        30.37D,
        30.36D
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

