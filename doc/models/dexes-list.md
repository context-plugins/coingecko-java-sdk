
# Dexes List

*This model accepts additional fields of type Object.*

## Structure

`DexesList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Data32>`](../../doc/models/data-32.md) | Required | - | List<Data32> getData() | setData(List<Data32> data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes17;
import com.coingecko.api.models.Data32;
import com.coingecko.api.models.DexesList;
import java.io.IOException;
import java.util.Arrays;

DexesList dexesList = new DexesList.Builder(
    Arrays.asList(
        new Data32.Builder(
            "id0",
            "type0",
            new Attributes17.Builder(
                "name4"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

