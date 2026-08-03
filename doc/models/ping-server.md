
# Ping Server

*This model accepts additional fields of type Object.*

## Structure

`PingServer`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GeckoSays` | `String` | Required | API server status message | String getGeckoSays() | setGeckoSays(String geckoSays) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.PingServer;
import java.io.IOException;

PingServer pingServer = new PingServer.Builder(
    "gecko_says6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

