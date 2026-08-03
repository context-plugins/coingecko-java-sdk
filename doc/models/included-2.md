
# Included 2

*This model accepts additional fields of type Object.*

## Structure

`Included2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `Attributes` | [`Attributes6`](../../doc/models/attributes-6.md) | Optional | - | Attributes6 getAttributes() | setAttributes(Attributes6 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes6;
import com.coingecko.api.models.Included2;
import java.io.IOException;

Included2 included2 = new Included2.Builder()
    .id("id6")
    .type("type6")
    .attributes(new Attributes6.Builder()
        .name("name4")
        .coingeckoAssetPlatformId("coingecko_asset_platform_id2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

