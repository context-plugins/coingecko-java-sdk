
# Data 33

*This model accepts additional fields of type Object.*

## Structure

`Data33`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Network identifier | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes18`](../../doc/models/attributes-18.md) | Required | - | Attributes18 getAttributes() | setAttributes(Attributes18 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes18;
import com.coingecko.api.models.Data33;
import java.io.IOException;

Data33 data33 = new Data33.Builder(
    "id2",
    "type2",
    new Attributes18.Builder(
        "name4",
        "coingecko_asset_platform_id2"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

