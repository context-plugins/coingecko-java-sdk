
# Data 9

*This model accepts additional fields of type Object.*

## Structure

`Data9`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Request ID | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes4`](../../doc/models/attributes-4.md) | Required | - | Attributes4 getAttributes() | setAttributes(Attributes4 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes4;
import com.coingecko.api.models.Data9;
import java.io.IOException;
import java.util.Arrays;

Data9 data9 = new Data9.Builder(
    "id4",
    "type6",
    new Attributes4.Builder(
        Arrays.asList(
            Arrays.asList(
                68.6D
            )
        )
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

