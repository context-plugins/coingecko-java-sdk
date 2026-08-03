
# Ticker

*This model accepts additional fields of type Object.*

## Structure

`Ticker`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Base` | `String` | Required | Ticker base currency | String getBase() | setBase(String base) |
| `Target` | `String` | Required | Ticker target currency | String getTarget() | setTarget(String target) |
| `Market` | [`Market`](../../doc/models/market.md) | Required | Exchange information | Market getMarket() | setMarket(Market market) |
| `Last` | [`double`](../../doc/models/precision.md) | Required | Last price | double getLast() | setLast(double last) |
| `Volume` | [`double`](../../doc/models/precision.md) | Required | Trading volume | double getVolume() | setVolume(double volume) |
| `CostToMoveUpUsd` | [`Double`](../../doc/models/precision.md) | Optional | Cost to move price up by 2% in USD | Double getCostToMoveUpUsd() | setCostToMoveUpUsd(Double costToMoveUpUsd) |
| `CostToMoveDownUsd` | [`Double`](../../doc/models/precision.md) | Optional | Cost to move price down by 2% in USD | Double getCostToMoveDownUsd() | setCostToMoveDownUsd(Double costToMoveDownUsd) |
| `ConvertedLast` | [`ConvertedLast`](../../doc/models/converted-last.md) | Required | Converted last price | ConvertedLast getConvertedLast() | setConvertedLast(ConvertedLast convertedLast) |
| `ConvertedVolume` | [`ConvertedVolume`](../../doc/models/converted-volume.md) | Required | Converted trading volume | ConvertedVolume getConvertedVolume() | setConvertedVolume(ConvertedVolume convertedVolume) |
| `TrustScore` | `String` | Required | Trust score | String getTrustScore() | setTrustScore(String trustScore) |
| `BidAskSpreadPercentage` | [`double`](../../doc/models/precision.md) | Required | Bid-ask spread percentage | double getBidAskSpreadPercentage() | setBidAskSpreadPercentage(double bidAskSpreadPercentage) |
| `Timestamp` | `String` | Required | Ticker timestamp | String getTimestamp() | setTimestamp(String timestamp) |
| `LastTradedAt` | `String` | Required | Last traded timestamp | String getLastTradedAt() | setLastTradedAt(String lastTradedAt) |
| `LastFetchAt` | `String` | Required | Last fetch timestamp | String getLastFetchAt() | setLastFetchAt(String lastFetchAt) |
| `IsAnomaly` | `boolean` | Required | Whether ticker is anomalous | boolean getIsAnomaly() | setIsAnomaly(boolean isAnomaly) |
| `IsStale` | `boolean` | Required | Whether ticker is stale | boolean getIsStale() | setIsStale(boolean isStale) |
| `TradeUrl` | `String` | Required | Trade URL | String getTradeUrl() | setTradeUrl(String tradeUrl) |
| `TokenInfoUrl` | `String` | Required | Token info URL | String getTokenInfoUrl() | setTokenInfoUrl(String tokenInfoUrl) |
| `CoinId` | `String` | Required | Base currency coin ID | String getCoinId() | setCoinId(String coinId) |
| `TargetCoinId` | `String` | Required | Target currency coin ID | String getTargetCoinId() | setTargetCoinId(String targetCoinId) |
| `CoinMcapUsd` | [`double`](../../doc/models/precision.md) | Required | Coin market cap in USD | double getCoinMcapUsd() | setCoinMcapUsd(double coinMcapUsd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ConvertedLast;
import com.coingecko.api.models.ConvertedVolume;
import com.coingecko.api.models.Market;
import com.coingecko.api.models.Ticker;
import java.io.IOException;

Ticker ticker = new Ticker.Builder(
    "base8",
    "target0",
    new Market.Builder()
        .name("name0")
        .identifier("identifier2")
        .hasTradingIncentive(false)
        .logo("logo6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    40.28D,
    95.58D,
    new ConvertedLast.Builder()
        .btc(30.96D)
        .eth(71.74D)
        .usd(5.04D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new ConvertedVolume.Builder()
        .btc(54.2D)
        .eth(94.98D)
        .usd(28.28D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "trust_score2",
    196.6D,
    "timestamp0",
    "last_traded_at6",
    "last_fetch_at2",
    false,
    false,
    "trade_url8",
    "token_info_url4",
    "coin_id8",
    "target_coin_id4",
    62.64D
)
.costToMoveUpUsd(61.48D)
.costToMoveDownUsd(246D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

