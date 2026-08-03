
# Ticker 1

*This model accepts additional fields of type Object.*

## Structure

`Ticker1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Base` | `String` | Optional | Ticker base currency | String getBase() | setBase(String base) |
| `Target` | `String` | Optional | Ticker target currency | String getTarget() | setTarget(String target) |
| `Market` | [`Market1`](../../doc/models/market-1.md) | Optional | Ticker exchange | Market1 getMarket() | setMarket(Market1 market) |
| `Last` | [`Double`](../../doc/models/precision.md) | Optional | Ticker last price | Double getLast() | setLast(Double last) |
| `Volume` | [`Double`](../../doc/models/precision.md) | Optional | Ticker volume | Double getVolume() | setVolume(Double volume) |
| `ConvertedLast` | [`ConvertedLast1`](../../doc/models/converted-last-1.md) | Optional | Ticker converted last price | ConvertedLast1 getConvertedLast() | setConvertedLast(ConvertedLast1 convertedLast) |
| `ConvertedVolume` | [`ConvertedVolume1`](../../doc/models/converted-volume-1.md) | Optional | Ticker converted volume | ConvertedVolume1 getConvertedVolume() | setConvertedVolume(ConvertedVolume1 convertedVolume) |
| `TrustScore` | `String` | Optional | Ticker trust score | String getTrustScore() | setTrustScore(String trustScore) |
| `BidAskSpreadPercentage` | [`Double`](../../doc/models/precision.md) | Optional | Ticker bid-ask spread percentage | Double getBidAskSpreadPercentage() | setBidAskSpreadPercentage(Double bidAskSpreadPercentage) |
| `Timestamp` | `String` | Optional | Ticker timestamp | String getTimestamp() | setTimestamp(String timestamp) |
| `LastTradedAt` | `String` | Optional | Ticker last traded timestamp | String getLastTradedAt() | setLastTradedAt(String lastTradedAt) |
| `LastFetchAt` | `String` | Optional | Ticker last fetch timestamp | String getLastFetchAt() | setLastFetchAt(String lastFetchAt) |
| `IsAnomaly` | `Boolean` | Optional | Ticker anomaly | Boolean getIsAnomaly() | setIsAnomaly(Boolean isAnomaly) |
| `IsStale` | `Boolean` | Optional | Ticker stale | Boolean getIsStale() | setIsStale(Boolean isStale) |
| `TradeUrl` | `String` | Optional | Ticker trade URL | String getTradeUrl() | setTradeUrl(String tradeUrl) |
| `TokenInfoUrl` | `String` | Optional | Ticker token info URL | String getTokenInfoUrl() | setTokenInfoUrl(String tokenInfoUrl) |
| `CoinId` | `String` | Optional | Ticker base currency coin ID | String getCoinId() | setCoinId(String coinId) |
| `TargetCoinId` | `String` | Optional | Ticker target currency coin ID | String getTargetCoinId() | setTargetCoinId(String targetCoinId) |
| `CoinMcapUsd` | [`Double`](../../doc/models/precision.md) | Optional | Market cap in USD | Double getCoinMcapUsd() | setCoinMcapUsd(Double coinMcapUsd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Market1;
import com.coingecko.api.models.Ticker1;
import java.io.IOException;

Ticker1 ticker1 = new Ticker1.Builder()
    .base("base0")
    .target("target8")
    .market(new Market1.Builder()
        .name("name0")
        .identifier("identifier2")
        .hasTradingIncentive(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .last(153.56D)
    .volume(238.3D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

