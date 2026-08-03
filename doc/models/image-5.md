
# Image 5

NFT collection image URLs

*This model accepts additional fields of type Object.*

## Structure

`Image5`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Small` | `String` | Optional | - | String getSmall() | setSmall(String small) |
| `Small2X` | `String` | Optional | - | String getSmall2X() | setSmall2X(String small2X) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Image5;
import java.io.IOException;

Image5 image5 = new Image5.Builder()
    .small("small6")
    .small2X("small_2x6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

