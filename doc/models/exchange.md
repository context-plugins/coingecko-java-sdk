
# Exchange

*This model accepts additional fields of type Object.*

## Structure

`Exchange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Exchange ID | String getId() | setId(String id) |
| `Name` | `String` | Required | Exchange name | String getName() | setName(String name) |
| `MarketType` | `String` | Required | Exchange market type | String getMarketType() | setMarketType(String marketType) |
| `Thumb` | `String` | Required | Exchange thumb image URL | String getThumb() | setThumb(String thumb) |
| `Large` | `String` | Required | Exchange large image URL | String getLarge() | setLarge(String large) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Exchange;
import java.io.IOException;

Exchange exchange = new Exchange.Builder(
    "id4",
    "name4",
    "market_type0",
    "thumb2",
    "large6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

