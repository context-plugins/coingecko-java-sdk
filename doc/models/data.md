
# Data

*This model accepts additional fields of type Object.*

## Structure

`Data`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ActiveCryptocurrencies` | `int` | Required | Number of active cryptocurrencies | int getActiveCryptocurrencies() | setActiveCryptocurrencies(int activeCryptocurrencies) |
| `UpcomingIcos` | `int` | Required | Number of upcoming ICOs | int getUpcomingIcos() | setUpcomingIcos(int upcomingIcos) |
| `OngoingIcos` | `int` | Required | Number of ongoing ICOs | int getOngoingIcos() | setOngoingIcos(int ongoingIcos) |
| `EndedIcos` | `int` | Required | Number of ended ICOs | int getEndedIcos() | setEndedIcos(int endedIcos) |
| `Markets` | `int` | Required | Number of exchanges | int getMarkets() | setMarkets(int markets) |
| `TotalMarketCap` | [`Map<String, Double>`](../../doc/models/precision.md) | Required | Total cryptocurrency market cap by currency | Map<String, Double> getTotalMarketCap() | setTotalMarketCap(Map<String, Double> totalMarketCap) |
| `TotalVolume` | [`Map<String, Double>`](../../doc/models/precision.md) | Required | Total cryptocurrency volume by currency | Map<String, Double> getTotalVolume() | setTotalVolume(Map<String, Double> totalVolume) |
| `MarketCapPercentage` | [`Map<String, Double>`](../../doc/models/precision.md) | Required | Market cap percentage by coin | Map<String, Double> getMarketCapPercentage() | setMarketCapPercentage(Map<String, Double> marketCapPercentage) |
| `MarketCapChangePercentage24HUsd` | [`double`](../../doc/models/precision.md) | Required | Market cap change percentage in 24 hours in USD | double getMarketCapChangePercentage24HUsd() | setMarketCapChangePercentage24HUsd(double marketCapChangePercentage24HUsd) |
| `VolumeChangePercentage24HUsd` | [`double`](../../doc/models/precision.md) | Required | Volume change percentage in 24 hours in USD | double getVolumeChangePercentage24HUsd() | setVolumeChangePercentage24HUsd(double volumeChangePercentage24HUsd) |
| `UpdatedAt` | `int` | Required | Last updated time in UNIX timestamp | int getUpdatedAt() | setUpdatedAt(int updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data;
import java.io.IOException;
import java.util.LinkedHashMap;

Data data = new Data.Builder(
    30,
    240,
    82,
    248,
    174,
    new LinkedHashMap<String, Double>() {{
        put("key0", 247.83D);
    }},
    new LinkedHashMap<String, Double>() {{
        put("key0", 99.58D);
        put("key1", 99.59D);
        put("key2", 99.6D);
    }},
    new LinkedHashMap<String, Double>() {{
        put("key0", 221.81D);
    }},
    5.14D,
    67.82D,
    120
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

