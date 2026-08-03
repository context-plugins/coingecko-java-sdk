
# Data 26

*This model accepts additional fields of type Object.*

## Structure

`Data26`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Pool identifier | String getId() | setId(String id) |
| `Type` | `String` | Required | Resource type | String getType() | setType(String type) |
| `Attributes` | [`Attributes14`](../../doc/models/attributes-14.md) | Required | - | Attributes14 getAttributes() | setAttributes(Attributes14 attributes) |
| `Relationships` | [`Relationships6`](../../doc/models/relationships-6.md) | Required | Related resources | Relationships6 getRelationships() | setRelationships(Relationships6 relationships) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes14;
import com.coingecko.api.models.BaseToken;
import com.coingecko.api.models.Data26;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Dex;
import com.coingecko.api.models.H1;
import com.coingecko.api.models.M5;
import com.coingecko.api.models.Network;
import com.coingecko.api.models.PriceChangePercentage;
import com.coingecko.api.models.QuoteToken;
import com.coingecko.api.models.Relationships6;
import com.coingecko.api.models.Transactions;
import com.coingecko.api.models.VolumeUsd;
import java.io.IOException;

Data26 data26 = new Data26.Builder(
    "id8",
    "type2",
    new Attributes14.Builder(
        "base_token_price_usd4",
        "base_token_price_native_currency6",
        "quote_token_price_usd8",
        "quote_token_price_native_currency2",
        "base_token_price_quote_token0",
        "quote_token_price_base_token6",
        "address0",
        "name4",
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
        "reserve_in_usd0"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new Relationships6.Builder()
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
        .network(new Network.Builder()
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
.build();
```

