
# Included

*This model accepts additional fields of type Object.*

## Structure

`Included`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `Attributes` | [`Attributes1`](../../doc/models/attributes-1.md) | Optional | - | Attributes1 getAttributes() | setAttributes(Attributes1 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes1;
import com.coingecko.api.models.Included;
import java.io.IOException;

Included included = new Included.Builder()
    .id("id2")
    .type("type8")
    .attributes(new Attributes1.Builder()
        .address("address0")
        .name("name4")
        .symbol("symbol6")
        .decimals(220)
        .imageUrl("image_url0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

