
# Image 3

Asset platform image URLs

*This model accepts additional fields of type Object.*

## Structure

`Image3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Thumb` | `String` | Optional | Thumbnail image URL | String getThumb() | setThumb(String thumb) |
| `Small` | `String` | Optional | Small image URL | String getSmall() | setSmall(String small) |
| `Large` | `String` | Optional | Large image URL | String getLarge() | setLarge(String large) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Image3;
import java.io.IOException;

Image3 image3 = new Image3.Builder()
    .thumb("thumb4")
    .small("small0")
    .large("large2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

