
# Links 2

NFT collection links

*This model accepts additional fields of type Object.*

## Structure

`Links2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Homepage` | `String` | Optional | - | String getHomepage() | setHomepage(String homepage) |
| `Twitter` | `String` | Optional | - | String getTwitter() | setTwitter(String twitter) |
| `Discord` | `String` | Optional | - | String getDiscord() | setDiscord(String discord) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Links2;
import java.io.IOException;

Links2 links2 = new Links2.Builder()
    .homepage("homepage0")
    .twitter("twitter0")
    .discord("discord4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

