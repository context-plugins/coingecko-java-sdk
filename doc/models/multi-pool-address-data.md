
# Multi Pool Address Data

*This model accepts additional fields of type Object.*

## Structure

`MultiPoolAddressData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<PoolAddressItem>`](../../doc/models/pool-address-item.md) | Required | - | List<PoolAddressItem> getData() | setData(List<PoolAddressItem> data) |
| `Included` | [`List<Included>`](../../doc/models/included.md) | Optional | Included related resources, present when include parameter is specified | List<Included> getIncluded() | setIncluded(List<Included> included) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes;
import com.coingecko.api.models.Attributes1;
import com.coingecko.api.models.BaseToken;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Dex;
import com.coingecko.api.models.H1;
import com.coingecko.api.models.Included;
import com.coingecko.api.models.M5;
import com.coingecko.api.models.MultiPoolAddressData;
import com.coingecko.api.models.NetBuyVolumeUsd;
import com.coingecko.api.models.PoolAddressItem;
import com.coingecko.api.models.PriceChangePercentage;
import com.coingecko.api.models.QuoteToken;
import com.coingecko.api.models.Relationships;
import com.coingecko.api.models.Transactions;
import com.coingecko.api.models.VolumeUsd;
import java.io.IOException;
import java.util.Arrays;

MultiPoolAddressData multiPoolAddressData = new MultiPoolAddressData.Builder(
    Arrays.asList(
        new PoolAddressItem.Builder(
            "id0",
            "type0",
            new Attributes.Builder(
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
            .build(),
            new Relationships.Builder()
                .baseToken(new BaseToken.Builder()
                    .data(new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .quoteToken(new QuoteToken.Builder()
                    .data(new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .dex(new Dex.Builder()
                    .data(new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.included(Arrays.asList(
        new Included.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes1.Builder()
                .address("address0")
                .name("name4")
                .symbol("symbol6")
                .decimals(220)
                .imageUrl("image_url0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Included.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes1.Builder()
                .address("address0")
                .name("name4")
                .symbol("symbol6")
                .decimals(220)
                .imageUrl("image_url0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Included.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes1.Builder()
                .address("address0")
                .name("name4")
                .symbol("symbol6")
                .decimals(220)
                .imageUrl("image_url0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

