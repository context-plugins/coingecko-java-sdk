
# Top Pools

*This model accepts additional fields of type Object.*

## Structure

`TopPools`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Data5>`](../../doc/models/data-5.md) | Optional | - | List<Data5> getData() | setData(List<Data5> data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.TopPools;
import java.io.IOException;
import java.util.Arrays;

TopPools topPools = new TopPools.Builder()
    .data(Arrays.asList(
        new Data5.Builder()
            .id("id0")
            .type("type0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

