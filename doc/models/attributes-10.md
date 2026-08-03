
# Attributes 10

*This model accepts additional fields of type Object.*

## Structure

`Attributes10`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BaseTokenPriceUsd` | `String` | Optional | - | String getBaseTokenPriceUsd() | setBaseTokenPriceUsd(String baseTokenPriceUsd) |
| `BaseTokenPriceNativeCurrency` | `String` | Optional | - | String getBaseTokenPriceNativeCurrency() | setBaseTokenPriceNativeCurrency(String baseTokenPriceNativeCurrency) |
| `QuoteTokenPriceUsd` | `String` | Optional | - | String getQuoteTokenPriceUsd() | setQuoteTokenPriceUsd(String quoteTokenPriceUsd) |
| `QuoteTokenPriceNativeCurrency` | `String` | Optional | - | String getQuoteTokenPriceNativeCurrency() | setQuoteTokenPriceNativeCurrency(String quoteTokenPriceNativeCurrency) |
| `BaseTokenPriceQuoteToken` | `String` | Optional | - | String getBaseTokenPriceQuoteToken() | setBaseTokenPriceQuoteToken(String baseTokenPriceQuoteToken) |
| `QuoteTokenPriceBaseToken` | `String` | Optional | - | String getQuoteTokenPriceBaseToken() | setQuoteTokenPriceBaseToken(String quoteTokenPriceBaseToken) |
| `Address` | `String` | Optional | - | String getAddress() | setAddress(String address) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `PoolCreatedAt` | `String` | Optional | - | String getPoolCreatedAt() | setPoolCreatedAt(String poolCreatedAt) |
| `FdvUsd` | `String` | Optional | - | String getFdvUsd() | setFdvUsd(String fdvUsd) |
| `MarketCapUsd` | `String` | Optional | - | String getMarketCapUsd() | setMarketCapUsd(String marketCapUsd) |
| `PriceChangePercentage` | [`PriceChangePercentage1`](../../doc/models/price-change-percentage-1.md) | Optional | - | PriceChangePercentage1 getPriceChangePercentage() | setPriceChangePercentage(PriceChangePercentage1 priceChangePercentage) |
| `Transactions` | [`Transactions1`](../../doc/models/transactions-1.md) | Optional | - | Transactions1 getTransactions() | setTransactions(Transactions1 transactions) |
| `VolumeUsd` | [`VolumeUsd2`](../../doc/models/volume-usd-2.md) | Optional | - | VolumeUsd2 getVolumeUsd() | setVolumeUsd(VolumeUsd2 volumeUsd) |
| `ReserveInUsd` | `String` | Optional | - | String getReserveInUsd() | setReserveInUsd(String reserveInUsd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes10;
import java.io.IOException;

Attributes10 attributes10 = new Attributes10.Builder()
    .baseTokenPriceUsd("base_token_price_usd2")
    .baseTokenPriceNativeCurrency("base_token_price_native_currency4")
    .quoteTokenPriceUsd("quote_token_price_usd4")
    .quoteTokenPriceNativeCurrency("quote_token_price_native_currency0")
    .baseTokenPriceQuoteToken("base_token_price_quote_token8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

