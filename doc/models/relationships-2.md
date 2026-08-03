
# Relationships 2

*This model accepts additional fields of type Object.*

## Structure

`Relationships2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pool` | [`Pool2`](../../doc/models/pool-2.md) | Optional | - | Pool2 getPool() | setPool(Pool2 pool) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Pool2;
import com.coingecko.api.models.Relationships2;
import java.io.IOException;

Relationships2 relationships2 = new Relationships2.Builder()
    .pool(new Pool2.Builder()
        .data(new Data5.Builder()
            .id("id0")
            .type("type0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

