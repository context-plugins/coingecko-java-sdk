
# Image

Coin image URLs

*This model accepts additional fields of type Object.*

## Structure

`Image`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Thumb` | `String` | Optional | Thumbnail image URL | String getThumb() | setThumb(String thumb) |
| `Small` | `String` | Optional | Small image URL | String getSmall() | setSmall(String small) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Image;
import java.io.IOException;

Image image = new Image.Builder()
    .thumb("thumb4")
    .small("small0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

