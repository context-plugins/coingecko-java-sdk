
# Attributes

*This model accepts additional fields of type Object.*

## Structure

`Attributes`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BaseTokenPriceUsd` | `String` | Required | Base token price in USD | String getBaseTokenPriceUsd() | setBaseTokenPriceUsd(String baseTokenPriceUsd) |
| `BaseTokenPriceNativeCurrency` | `String` | Required | Base token price in native currency | String getBaseTokenPriceNativeCurrency() | setBaseTokenPriceNativeCurrency(String baseTokenPriceNativeCurrency) |
| `BaseTokenBalance` | `String` | Optional | Base token balance in pool | String getBaseTokenBalance() | setBaseTokenBalance(String baseTokenBalance) |
| `BaseTokenLiquidityUsd` | `String` | Optional | Base token liquidity in USD | String getBaseTokenLiquidityUsd() | setBaseTokenLiquidityUsd(String baseTokenLiquidityUsd) |
| `QuoteTokenPriceUsd` | `String` | Required | Quote token price in USD | String getQuoteTokenPriceUsd() | setQuoteTokenPriceUsd(String quoteTokenPriceUsd) |
| `QuoteTokenPriceNativeCurrency` | `String` | Required | Quote token price in native currency | String getQuoteTokenPriceNativeCurrency() | setQuoteTokenPriceNativeCurrency(String quoteTokenPriceNativeCurrency) |
| `QuoteTokenBalance` | `String` | Optional | Quote token balance in pool | String getQuoteTokenBalance() | setQuoteTokenBalance(String quoteTokenBalance) |
| `QuoteTokenLiquidityUsd` | `String` | Optional | Quote token liquidity in USD | String getQuoteTokenLiquidityUsd() | setQuoteTokenLiquidityUsd(String quoteTokenLiquidityUsd) |
| `BaseTokenPriceQuoteToken` | `String` | Required | Base token price in quote token | String getBaseTokenPriceQuoteToken() | setBaseTokenPriceQuoteToken(String baseTokenPriceQuoteToken) |
| `QuoteTokenPriceBaseToken` | `String` | Required | Quote token price in base token | String getQuoteTokenPriceBaseToken() | setQuoteTokenPriceBaseToken(String quoteTokenPriceBaseToken) |
| `Address` | `String` | Required | Pool contract address | String getAddress() | setAddress(String address) |
| `Name` | `String` | Required | Pool name with fee tier | String getName() | setName(String name) |
| `PoolName` | `String` | Required | Pool name without fee tier | String getPoolName() | setPoolName(String poolName) |
| `PoolFeePercentage` | `String` | Required | Pool fee percentage | String getPoolFeePercentage() | setPoolFeePercentage(String poolFeePercentage) |
| `PoolCreatedAt` | `String` | Required | Pool creation timestamp | String getPoolCreatedAt() | setPoolCreatedAt(String poolCreatedAt) |
| `FdvUsd` | `String` | Required | Fully diluted valuation in USD | String getFdvUsd() | setFdvUsd(String fdvUsd) |
| `MarketCapUsd` | `String` | Required | Market cap in USD | String getMarketCapUsd() | setMarketCapUsd(String marketCapUsd) |
| `PriceChangePercentage` | [`PriceChangePercentage`](../../doc/models/price-change-percentage.md) | Required | Price change percentage over various timeframes | PriceChangePercentage getPriceChangePercentage() | setPriceChangePercentage(PriceChangePercentage priceChangePercentage) |
| `Transactions` | [`Transactions`](../../doc/models/transactions.md) | Required | Transaction counts over various timeframes | Transactions getTransactions() | setTransactions(Transactions transactions) |
| `VolumeUsd` | [`VolumeUsd`](../../doc/models/volume-usd.md) | Required | Volume in USD over various timeframes | VolumeUsd getVolumeUsd() | setVolumeUsd(VolumeUsd volumeUsd) |
| `NetBuyVolumeUsd` | [`NetBuyVolumeUsd`](../../doc/models/net-buy-volume-usd.md) | Optional | Net buy volume in USD over various timeframes | NetBuyVolumeUsd getNetBuyVolumeUsd() | setNetBuyVolumeUsd(NetBuyVolumeUsd netBuyVolumeUsd) |
| `BuyVolumeUsd` | [`BuyVolumeUsd`](../../doc/models/buy-volume-usd.md) | Optional | Buy volume in USD over various timeframes | BuyVolumeUsd getBuyVolumeUsd() | setBuyVolumeUsd(BuyVolumeUsd buyVolumeUsd) |
| `SellVolumeUsd` | [`SellVolumeUsd`](../../doc/models/sell-volume-usd.md) | Optional | Sell volume in USD over various timeframes | SellVolumeUsd getSellVolumeUsd() | setSellVolumeUsd(SellVolumeUsd sellVolumeUsd) |
| `ReserveInUsd` | `String` | Required | Total reserve in USD | String getReserveInUsd() | setReserveInUsd(String reserveInUsd) |
| `LockedLiquidityPercentage` | `String` | Required | Locked liquidity percentage | String getLockedLiquidityPercentage() | setLockedLiquidityPercentage(String lockedLiquidityPercentage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes;
import com.coingecko.api.models.H1;
import com.coingecko.api.models.M5;
import com.coingecko.api.models.NetBuyVolumeUsd;
import com.coingecko.api.models.PriceChangePercentage;
import com.coingecko.api.models.Transactions;
import com.coingecko.api.models.VolumeUsd;
import java.io.IOException;

Attributes attributes = new Attributes.Builder(
    "base_token_price_usd4",
    "base_token_price_native_currency6",
    "quote_token_price_usd8",
    "quote_token_price_native_currency2",
    "base_token_price_quote_token0",
    "quote_token_price_base_token6",
    "address0",
    "name4",
    "pool_name8",
    "pool_fee_percentage8",
    "pool_created_at6",
    "fdv_usd8",
    "market_cap_usd0",
    new PriceChangePercentage.Builder()
        .m5("m50")
        .m15("m156")
        .m30("m306")
        .h1("h10")
        .h6("h62")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new Transactions.Builder()
        .m5(new M5.Builder()
            .buys(154)
            .sells(38)
            .buyers(224)
            .sellers(100)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .m15(new M5.Builder()
            .buys(240)
            .sells(100)
            .buyers(106)
            .sellers(38)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .m30(new M5.Builder()
            .buys(172)
            .sells(32)
            .buyers(38)
            .sellers(226)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .h1(new H1.Builder()
            .buys(216)
            .sells(76)
            .buyers(82)
            .sellers(14)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .h6(new H1.Builder()
            .buys(32)
            .sells(148)
            .buyers(154)
            .sellers(170)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    new VolumeUsd.Builder()
        .m5("m56")
        .m15("m150")
        .m30("m302")
        .h1("h16")
        .h6("h68")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
    "reserve_in_usd0",
    "locked_liquidity_percentage2"
)
.baseTokenBalance("base_token_balance6")
.baseTokenLiquidityUsd("base_token_liquidity_usd0")
.quoteTokenBalance("quote_token_balance8")
.quoteTokenLiquidityUsd("quote_token_liquidity_usd8")
.netBuyVolumeUsd(new NetBuyVolumeUsd.Builder()
        .m5("m52")
        .m15("m154")
        .m30("m308")
        .h1("h12")
        .h6("h64")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

