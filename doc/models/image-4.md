
# Image 4

Project image URLs

*This model accepts additional fields of type Object.*

## Structure

`Image4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Thumb` | `String` | Optional | - | String getThumb() | setThumb(String thumb) |
| `Small` | `String` | Optional | - | String getSmall() | setSmall(String small) |
| `Large` | `String` | Optional | - | String getLarge() | setLarge(String large) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Image4;
import java.io.IOException;

Image4 image4 = new Image4.Builder()
    .thumb("thumb2")
    .small("small8")
    .large("large4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

