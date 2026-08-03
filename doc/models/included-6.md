
# Included 6

*This model accepts additional fields of type Object.*

## Structure

`Included6`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `Attributes` | [`Attributes13`](../../doc/models/attributes-13.md) | Optional | - | Attributes13 getAttributes() | setAttributes(Attributes13 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes13;
import com.coingecko.api.models.Included6;
import java.io.IOException;

Included6 included6 = new Included6.Builder()
    .id("id6")
    .type("type4")
    .attributes(new Attributes13.Builder()
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

