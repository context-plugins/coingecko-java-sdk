
# Public Interest Stats

Public interest statistics

*This model accepts additional fields of type Object.*

## Structure

`PublicInterestStats`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AlexaRank` | [`Double`](../../doc/models/precision.md) | Optional | Alexa rank | Double getAlexaRank() | setAlexaRank(Double alexaRank) |
| `BingMatches` | [`Double`](../../doc/models/precision.md) | Optional | Bing search matches | Double getBingMatches() | setBingMatches(Double bingMatches) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.PublicInterestStats;
import java.io.IOException;

PublicInterestStats publicInterestStats = new PublicInterestStats.Builder()
    .alexaRank(182.32D)
    .bingMatches(160.54D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

