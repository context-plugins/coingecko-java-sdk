
# Attributes 9

*This model accepts additional fields of type Object.*

## Structure

`Attributes9`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Required | Token contract address | String getAddress() | setAddress(String address) |
| `Name` | `String` | Required | Token name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | Token symbol | String getSymbol() | setSymbol(String symbol) |
| `Decimals` | `int` | Required | Token decimals | int getDecimals() | setDecimals(int decimals) |
| `ImageUrl` | `String` | Required | Token image URL | String getImageUrl() | setImageUrl(String imageUrl) |
| `CoingeckoCoinId` | `String` | Required | CoinGecko coin ID | String getCoingeckoCoinId() | setCoingeckoCoinId(String coingeckoCoinId) |
| `TotalSupply` | `String` | Required | Token total supply | String getTotalSupply() | setTotalSupply(String totalSupply) |
| `NormalizedTotalSupply` | `String` | Required | Normalized token total supply | String getNormalizedTotalSupply() | setNormalizedTotalSupply(String normalizedTotalSupply) |
| `PriceUsd` | `String` | Required | Token price in USD | String getPriceUsd() | setPriceUsd(String priceUsd) |
| `FdvUsd` | `String` | Required | Fully diluted valuation in USD | String getFdvUsd() | setFdvUsd(String fdvUsd) |
| `TotalReserveInUsd` | `String` | Required | Total reserve in USD across all pools | String getTotalReserveInUsd() | setTotalReserveInUsd(String totalReserveInUsd) |
| `VolumeUsd` | [`VolumeUsd1`](../../doc/models/volume-usd-1.md) | Required | Volume in USD | VolumeUsd1 getVolumeUsd() | setVolumeUsd(VolumeUsd1 volumeUsd) |
| `MarketCapUsd` | `String` | Required | Market cap in USD | String getMarketCapUsd() | setMarketCapUsd(String marketCapUsd) |
| `LastTradeTimestamp` | `String` | Optional | Last trade timestamp in UNIX | String getLastTradeTimestamp() | setLastTradeTimestamp(String lastTradeTimestamp) |
| `LaunchpadDetails` | [`LaunchpadDetails`](../../doc/models/launchpad-details.md) | Optional | Launchpad details for pump-style tokens | LaunchpadDetails getLaunchpadDetails() | setLaunchpadDetails(LaunchpadDetails launchpadDetails) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes9;
import com.coingecko.api.models.LaunchpadDetails;
import com.coingecko.api.models.VolumeUsd1;
import java.io.IOException;

Attributes9 attributes9 = new Attributes9.Builder(
    "address6",
    "name0",
    "symbol8",
    12,
    "image_url6",
    "coingecko_coin_id8",
    "total_supply2",
    "normalized_total_supply0",
    "price_usd4",
    "fdv_usd4",
    "total_reserve_in_usd0",
    new VolumeUsd1.Builder()
        .h24("h242")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "market_cap_usd6"
)
.lastTradeTimestamp("last_trade_timestamp0")
.launchpadDetails(new LaunchpadDetails.Builder()
        .graduationPercentage(93.02D)
        .completed(false)
        .completedAt("completed_at4")
        .migratedDestinationPoolAddress("migrated_destination_pool_address8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

