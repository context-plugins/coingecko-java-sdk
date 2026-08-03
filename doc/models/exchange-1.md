
# Exchange 1

*This model accepts additional fields of type Object.*

## Structure

`Exchange1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Exchange ID | String getId() | setId(String id) |
| `Name` | `String` | Required | Exchange name | String getName() | setName(String name) |
| `YearEstablished` | [`Double`](../../doc/models/precision.md) | Required | Year the exchange was established | Double getYearEstablished() | setYearEstablished(Double yearEstablished) |
| `Country` | `String` | Required | Country where the exchange is based | String getCountry() | setCountry(String country) |
| `Description` | `String` | Required | Exchange description | String getDescription() | setDescription(String description) |
| `Url` | `String` | Required | Exchange website URL | String getUrl() | setUrl(String url) |
| `Image` | `String` | Required | Exchange logo URL | String getImage() | setImage(String image) |
| `HasTradingIncentive` | `boolean` | Required | Whether the exchange has trading incentive | boolean getHasTradingIncentive() | setHasTradingIncentive(boolean hasTradingIncentive) |
| `TrustScore` | [`Double`](../../doc/models/precision.md) | Required | Exchange trust score | Double getTrustScore() | setTrustScore(Double trustScore) |
| `TrustScoreRank` | [`Double`](../../doc/models/precision.md) | Required | Exchange trust score rank | Double getTrustScoreRank() | setTrustScoreRank(Double trustScoreRank) |
| `TradeVolume24HBtc` | [`double`](../../doc/models/precision.md) | Required | Exchange 24h trading volume in BTC | double getTradeVolume24HBtc() | setTradeVolume24HBtc(double tradeVolume24HBtc) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Exchange1;
import java.io.IOException;

Exchange1 exchange1 = new Exchange1.Builder(
    "id8",
    "name8",
    37.94D,
    "country2",
    "description8",
    "url2",
    "image8",
    false,
    65.08D,
    161.9D,
    155.02D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

