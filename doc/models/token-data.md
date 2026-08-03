
# Token Data

*This model accepts additional fields of type Object.*

## Structure

`TokenData`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`TokenItem`](../../doc/models/token-item.md) | Required | - | TokenItem getData() | setData(TokenItem data) |
| `Included` | [`List<Included5>`](../../doc/models/included-5.md) | Optional | Included top pool data, present when include=top_pools is specified | List<Included5> getIncluded() | setIncluded(List<Included5> included) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes11;
import com.coingecko.api.models.Attributes9;
import com.coingecko.api.models.BaseToken;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Dex;
import com.coingecko.api.models.Included5;
import com.coingecko.api.models.LaunchpadDetails;
import com.coingecko.api.models.QuoteToken;
import com.coingecko.api.models.Relationships3;
import com.coingecko.api.models.Relationships4;
import com.coingecko.api.models.TokenData;
import com.coingecko.api.models.TokenItem;
import com.coingecko.api.models.TopPools;
import com.coingecko.api.models.VolumeUsd1;
import java.io.IOException;
import java.util.Arrays;

TokenData tokenData = new TokenData.Builder(
    new TokenItem.Builder(
        "id0",
        "type0",
        new Attributes9.Builder(
            "address0",
            "name4",
            "symbol6",
            220,
            "image_url0",
            "coingecko_coin_id4",
            "total_supply2",
            "normalized_total_supply4",
            "price_usd8",
            "fdv_usd8",
            "total_reserve_in_usd4",
            new VolumeUsd1.Builder()
                .h24("h242")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build(),
            "market_cap_usd0"
        )
        .lastTradeTimestamp("last_trade_timestamp4")
        .launchpadDetails(new LaunchpadDetails.Builder()
                .graduationPercentage(93.02D)
                .completed(false)
                .completedAt("completed_at4")
                .migratedDestinationPoolAddress("migrated_destination_pool_address8")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Relationships3.Builder()
            .topPools(new TopPools.Builder()
                .data(Arrays.asList(
                    new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                    new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                ))
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.included(Arrays.asList(
        new Included5.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes11.Builder()
                .baseTokenPriceUsd("base_token_price_usd4")
                .baseTokenPriceNativeCurrency("base_token_price_native_currency6")
                .quoteTokenPriceUsd("quote_token_price_usd8")
                .quoteTokenPriceNativeCurrency("quote_token_price_native_currency2")
                .baseTokenPriceQuoteToken("base_token_price_quote_token0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .relationships(new Relationships4.Builder()
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
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Included5.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes11.Builder()
                .baseTokenPriceUsd("base_token_price_usd4")
                .baseTokenPriceNativeCurrency("base_token_price_native_currency6")
                .quoteTokenPriceUsd("quote_token_price_usd8")
                .quoteTokenPriceNativeCurrency("quote_token_price_native_currency2")
                .baseTokenPriceQuoteToken("base_token_price_quote_token0")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .relationships(new Relationships4.Builder()
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
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

