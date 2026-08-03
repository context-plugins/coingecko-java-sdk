
# Networks List

*This model accepts additional fields of type Object.*

## Structure

`NetworksList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Data33>`](../../doc/models/data-33.md) | Required | - | List<Data33> getData() | setData(List<Data33> data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes18;
import com.coingecko.api.models.Data33;
import com.coingecko.api.models.NetworksList;
import java.io.IOException;
import java.util.Arrays;

NetworksList networksList = new NetworksList.Builder(
    Arrays.asList(
        new Data33.Builder(
            "id0",
            "type0",
            new Attributes18.Builder(
                "name4",
                "coingecko_asset_platform_id2"
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

