
# Coin

*This model accepts additional fields of type Object.*

## Structure

`Coin`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Coin ID | String getId() | setId(String id) |
| `Name` | `String` | Required | Coin name | String getName() | setName(String name) |
| `ApiSymbol` | `String` | Required | Coin API symbol | String getApiSymbol() | setApiSymbol(String apiSymbol) |
| `Symbol` | `String` | Required | Coin symbol | String getSymbol() | setSymbol(String symbol) |
| `MarketCapRank` | `Integer` | Required | Coin market cap rank | Integer getMarketCapRank() | setMarketCapRank(Integer marketCapRank) |
| `Thumb` | `String` | Required | Coin thumb image URL | String getThumb() | setThumb(String thumb) |
| `Large` | `String` | Required | Coin large image URL | String getLarge() | setLarge(String large) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Coin;
import java.io.IOException;

Coin coin = new Coin.Builder(
    "id4",
    "name4",
    "api_symbol2",
    "symbol6",
    238,
    "thumb2",
    "large6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

