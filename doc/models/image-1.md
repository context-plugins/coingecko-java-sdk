
# Image 1

Coin image URL

*This model accepts additional fields of type Object.*

## Structure

`Image1`

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
import com.coingecko.api.models.Image1;
import java.io.IOException;

Image1 image1 = new Image1.Builder()
    .thumb("thumb6")
    .small("small2")
    .large("large0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

