
# Coins List

*This model accepts additional fields of type Object.*

## Structure

`CoinsList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `Platforms` | `Map<String, String>` | Optional | Asset platform and contract address | Map<String, String> getPlatforms() | setPlatforms(Map<String, String> platforms) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CoinsList;
import java.io.IOException;
import java.util.LinkedHashMap;

CoinsList coinsList = new CoinsList.Builder(
    "id4",
    "symbol4",
    "name4"
)
.platforms(new LinkedHashMap<String, String>() {{
        put("key0", "platforms9");
        put("key1", "platforms8");
        put("key2", "platforms7");
    }})
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

