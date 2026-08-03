
# Ticker 3

*This model accepts additional fields of type Object.*

## Structure

`Ticker3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Base` | `String` | Optional | Ticker base currency | String getBase() | setBase(String base) |
| `Target` | `String` | Optional | Ticker target currency | String getTarget() | setTarget(String target) |
| `Market` | [`Market3`](../../doc/models/market-3.md) | Optional | Exchange information | Market3 getMarket() | setMarket(Market3 market) |
| `Last` | [`Double`](../../doc/models/precision.md) | Optional | Last price | Double getLast() | setLast(Double last) |
| `Volume` | [`Double`](../../doc/models/precision.md) | Optional | Trading volume | Double getVolume() | setVolume(Double volume) |
| `ConvertedLast` | [`ConvertedLast`](../../doc/models/converted-last.md) | Optional | Converted last price | ConvertedLast getConvertedLast() | setConvertedLast(ConvertedLast convertedLast) |
| `ConvertedVolume` | [`ConvertedVolume`](../../doc/models/converted-volume.md) | Optional | Converted trading volume | ConvertedVolume getConvertedVolume() | setConvertedVolume(ConvertedVolume convertedVolume) |
| `TrustScore` | `String` | Optional | Trust score | String getTrustScore() | setTrustScore(String trustScore) |
| `BidAskSpreadPercentage` | [`Double`](../../doc/models/precision.md) | Optional | Bid-ask spread percentage | Double getBidAskSpreadPercentage() | setBidAskSpreadPercentage(Double bidAskSpreadPercentage) |
| `Timestamp` | `String` | Optional | Ticker timestamp | String getTimestamp() | setTimestamp(String timestamp) |
| `LastTradedAt` | `String` | Optional | Last traded timestamp | String getLastTradedAt() | setLastTradedAt(String lastTradedAt) |
| `LastFetchAt` | `String` | Optional | Last fetch timestamp | String getLastFetchAt() | setLastFetchAt(String lastFetchAt) |
| `IsAnomaly` | `Boolean` | Optional | Whether ticker is anomalous | Boolean getIsAnomaly() | setIsAnomaly(Boolean isAnomaly) |
| `IsStale` | `Boolean` | Optional | Whether ticker is stale | Boolean getIsStale() | setIsStale(Boolean isStale) |
| `TradeUrl` | `String` | Optional | Trade URL | String getTradeUrl() | setTradeUrl(String tradeUrl) |
| `TokenInfoUrl` | `String` | Optional | Token info URL | String getTokenInfoUrl() | setTokenInfoUrl(String tokenInfoUrl) |
| `CoinId` | `String` | Optional | Base currency coin ID | String getCoinId() | setCoinId(String coinId) |
| `TargetCoinId` | `String` | Optional | Target currency coin ID | String getTargetCoinId() | setTargetCoinId(String targetCoinId) |
| `CoinMcapUsd` | [`Double`](../../doc/models/precision.md) | Optional | Coin market cap in USD | Double getCoinMcapUsd() | setCoinMcapUsd(Double coinMcapUsd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Market3;
import com.coingecko.api.models.Ticker3;
import java.io.IOException;

Ticker3 ticker3 = new Ticker3.Builder()
    .base("base6")
    .target("target8")
    .market(new Market3.Builder()
        .name("name0")
        .identifier("identifier2")
        .hasTradingIncentive(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .last(154.6D)
    .volume(34.46D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

