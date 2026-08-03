
# Project

Project information

*This model accepts additional fields of type Object.*

## Structure

`Project`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | `String` | Optional | Project type | String getType() | setType(String type) |
| `Id` | `String` | Optional | Project ID | String getId() | setId(String id) |
| `Name` | `String` | Optional | Project name | String getName() | setName(String name) |
| `Image` | [`Image4`](../../doc/models/image-4.md) | Optional | Project image URLs | Image4 getImage() | setImage(Image4 image) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Image4;
import com.coingecko.api.models.Project;
import java.io.IOException;

Project project = new Project.Builder()
    .type("type4")
    .id("id6")
    .name("name6")
    .image(new Image4.Builder()
        .thumb("thumb4")
        .small("small0")
        .large("large8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

