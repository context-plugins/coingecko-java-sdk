
# Relationships 3

*This model accepts additional fields of type Object.*

## Structure

`Relationships3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TopPools` | [`TopPools`](../../doc/models/top-pools.md) | Optional | - | TopPools getTopPools() | setTopPools(TopPools topPools) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Relationships3;
import com.coingecko.api.models.TopPools;
import java.io.IOException;
import java.util.Arrays;

Relationships3 relationships3 = new Relationships3.Builder()
    .topPools(new TopPools.Builder()
        .data(Arrays.asList(
            new Data5.Builder()
                .id("id0")
                .type("type0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            new Data5.Builder()
                .id("id0")
                .type("type0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

