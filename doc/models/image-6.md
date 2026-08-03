
# Image 6

Token image URLs in different sizes

*This model accepts additional fields of type Object.*

## Structure

`Image6`

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
import com.coingecko.api.models.Image6;
import java.io.IOException;

Image6 image6 = new Image6.Builder()
    .thumb("thumb4")
    .small("small0")
    .large("large2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

