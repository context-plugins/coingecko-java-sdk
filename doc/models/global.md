
# Global

*This model accepts additional fields of type Object.*

## Structure

`Global`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Data`](../../doc/models/data.md) | Required | - | Data getData() | setData(Data data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data;
import com.coingecko.api.models.Global;
import java.io.IOException;
import java.util.LinkedHashMap;

Global global = new Global.Builder(
    new Data.Builder(
        30,
        240,
        82,
        248,
        174,
        new LinkedHashMap<String, Double>() {{
            put("key0", 247.83D);
        }},
        new LinkedHashMap<String, Double>() {{
            put("key0", 99.58D);
            put("key1", 99.59D);
            put("key2", 99.6D);
        }},
        new LinkedHashMap<String, Double>() {{
            put("key0", 221.81D);
        }},
        5.14D,
        67.82D,
        120
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

