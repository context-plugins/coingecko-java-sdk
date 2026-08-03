
# Data 32

*This model accepts additional fields of type Object.*

## Structure

`Data32`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | DEX identifier | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes17`](../../doc/models/attributes-17.md) | Required | - | Attributes17 getAttributes() | setAttributes(Attributes17 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes17;
import com.coingecko.api.models.Data32;
import java.io.IOException;

Data32 data32 = new Data32.Builder(
    "id2",
    "type2",
    new Attributes17.Builder(
        "name4"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

