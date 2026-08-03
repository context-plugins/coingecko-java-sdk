
# Data 1

*This model accepts additional fields of type Object.*

## Structure

`Data1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DefiMarketCap` | `String` | Required | DeFi market cap | String getDefiMarketCap() | setDefiMarketCap(String defiMarketCap) |
| `EthMarketCap` | `String` | Required | ETH market cap | String getEthMarketCap() | setEthMarketCap(String ethMarketCap) |
| `DefiToEthRatio` | `String` | Required | DeFi to ETH ratio | String getDefiToEthRatio() | setDefiToEthRatio(String defiToEthRatio) |
| `TradingVolume24H` | `String` | Required | DeFi trading volume in 24 hours | String getTradingVolume24H() | setTradingVolume24H(String tradingVolume24H) |
| `DefiDominance` | `String` | Required | DeFi dominance percentage | String getDefiDominance() | setDefiDominance(String defiDominance) |
| `TopCoinName` | `String` | Required | DeFi top coin name | String getTopCoinName() | setTopCoinName(String topCoinName) |
| `TopCoinDefiDominance` | [`double`](../../doc/models/precision.md) | Required | DeFi top coin dominance percentage | double getTopCoinDefiDominance() | setTopCoinDefiDominance(double topCoinDefiDominance) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data1;
import java.io.IOException;

Data1 data1 = new Data1.Builder(
    "defi_market_cap4",
    "eth_market_cap8",
    "defi_to_eth_ratio8",
    "trading_volume_24h2",
    "defi_dominance6",
    "top_coin_name0",
    63D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

