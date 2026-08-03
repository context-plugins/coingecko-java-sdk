
# Derivatives Exchange

*This model accepts additional fields of type Object.*

## Structure

`DerivativesExchange`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Derivatives exchange name | String getName() | setName(String name) |
| `Id` | `String` | Required | Derivatives exchange ID | String getId() | setId(String id) |
| `OpenInterestBtc` | [`double`](../../doc/models/precision.md) | Required | Derivatives exchange open interest in BTC | double getOpenInterestBtc() | setOpenInterestBtc(double openInterestBtc) |
| `TradeVolume24HBtc` | `String` | Required | Derivatives exchange trade volume in BTC in 24 hours | String getTradeVolume24HBtc() | setTradeVolume24HBtc(String tradeVolume24HBtc) |
| `NumberOfPerpetualPairs` | `int` | Required | Number of perpetual pairs in the derivatives exchange | int getNumberOfPerpetualPairs() | setNumberOfPerpetualPairs(int numberOfPerpetualPairs) |
| `NumberOfFuturesPairs` | `int` | Required | Number of futures pairs in the derivatives exchange | int getNumberOfFuturesPairs() | setNumberOfFuturesPairs(int numberOfFuturesPairs) |
| `Image` | `String` | Required | Derivatives exchange image URL | String getImage() | setImage(String image) |
| `YearEstablished` | `Integer` | Required | Derivatives exchange established year | Integer getYearEstablished() | setYearEstablished(Integer yearEstablished) |
| `Country` | `String` | Required | Derivatives exchange incorporated country | String getCountry() | setCountry(String country) |
| `Description` | `String` | Required | Derivatives exchange description | String getDescription() | setDescription(String description) |
| `Url` | `String` | Required | Derivatives exchange website URL | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DerivativesExchange;
import java.io.IOException;

DerivativesExchange derivativesExchange = new DerivativesExchange.Builder(
    "name8",
    "id8",
    68.38D,
    "trade_volume_24h_btc2",
    148,
    128,
    "image8",
    36,
    "country2",
    "description8",
    "url2"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

