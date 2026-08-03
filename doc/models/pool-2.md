
# Pool 2

*This model accepts additional fields of type Object.*

## Structure

`Pool2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Data5`](../../doc/models/data-5.md) | Optional | - | Data5 getData() | setData(Data5 data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Pool2;
import java.io.IOException;

Pool2 pool2 = new Pool2.Builder()
    .data(new Data5.Builder()
        .id("id0")
        .type("type0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

