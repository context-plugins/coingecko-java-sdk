
# Ticker 4

*This model accepts additional fields of type Object.*

## Structure

`Ticker4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Symbol` | `String` | Required | Derivative ticker symbol | String getSymbol() | setSymbol(String symbol) |
| `Base` | `String` | Required | Derivative base asset | String getBase() | setBase(String base) |
| `Target` | `String` | Required | Derivative target asset | String getTarget() | setTarget(String target) |
| `CoinId` | `String` | Required | Derivative base asset coin ID | String getCoinId() | setCoinId(String coinId) |
| `TargetCoinId` | `String` | Required | Derivative target asset coin ID | String getTargetCoinId() | setTargetCoinId(String targetCoinId) |
| `TradeUrl` | `String` | Required | Derivative trade URL | String getTradeUrl() | setTradeUrl(String tradeUrl) |
| `ContractType` | `String` | Required | Derivative contract type | String getContractType() | setContractType(String contractType) |
| `Last` | [`double`](../../doc/models/precision.md) | Required | Derivative last price | double getLast() | setLast(double last) |
| `H24PercentageChange` | [`double`](../../doc/models/precision.md) | Required | Derivative price percentage change in 24 hours | double getH24PercentageChange() | setH24PercentageChange(double h24PercentageChange) |
| `Index` | [`double`](../../doc/models/precision.md) | Required | Derivative underlying asset price | double getIndex() | setIndex(double index) |
| `IndexBasisPercentage` | [`double`](../../doc/models/precision.md) | Required | Difference of derivative price and index price in percentage | double getIndexBasisPercentage() | setIndexBasisPercentage(double indexBasisPercentage) |
| `BidAskSpread` | [`double`](../../doc/models/precision.md) | Required | Derivative bid-ask spread | double getBidAskSpread() | setBidAskSpread(double bidAskSpread) |
| `FundingRate` | [`double`](../../doc/models/precision.md) | Required | Derivative funding rate | double getFundingRate() | setFundingRate(double fundingRate) |
| `OpenInterestUsd` | [`double`](../../doc/models/precision.md) | Required | Derivative open interest in USD | double getOpenInterestUsd() | setOpenInterestUsd(double openInterestUsd) |
| `H24Volume` | [`double`](../../doc/models/precision.md) | Required | Derivative volume in 24 hours | double getH24Volume() | setH24Volume(double h24Volume) |
| `ConvertedVolume` | [`ConvertedVolume4`](../../doc/models/converted-volume-4.md) | Required | Derivative converted volume | ConvertedVolume4 getConvertedVolume() | setConvertedVolume(ConvertedVolume4 convertedVolume) |
| `ConvertedLast` | [`ConvertedLast4`](../../doc/models/converted-last-4.md) | Required | Derivative converted last price | ConvertedLast4 getConvertedLast() | setConvertedLast(ConvertedLast4 convertedLast) |
| `LastTraded` | [`double`](../../doc/models/precision.md) | Required | Derivative last traded time in UNIX timestamp | double getLastTraded() | setLastTraded(double lastTraded) |
| `ExpiredAt` | [`Double`](../../doc/models/precision.md) | Required | Derivative expiry time in UNIX timestamp | Double getExpiredAt() | setExpiredAt(Double expiredAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ConvertedLast4;
import com.coingecko.api.models.ConvertedVolume4;
import com.coingecko.api.models.Ticker4;
import java.io.IOException;

Ticker4 ticker4 = new Ticker4.Builder(
    "symbol0",
    "base4",
    "target6",
    "coin_id4",
    "target_coin_id0",
    "trade_url4",
    "contract_type6",
    148.48D,
    197.94D,
    36.76D,
    107.36D,
    234.44D,
    79.9D,
    55.46D,
    103.96D,
    new ConvertedVolume4.Builder()
        .btc("btc0")
        .eth("eth8")
        .usd("usd8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new ConvertedLast4.Builder()
        .btc("btc6")
        .eth("eth4")
        .usd("usd4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    143.96D,
    249.88D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

