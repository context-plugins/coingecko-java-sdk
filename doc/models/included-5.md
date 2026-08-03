
# Included 5

*This model accepts additional fields of type Object.*

## Structure

`Included5`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `Attributes` | [`Attributes11`](../../doc/models/attributes-11.md) | Optional | - | Attributes11 getAttributes() | setAttributes(Attributes11 attributes) |
| `Relationships` | [`Relationships4`](../../doc/models/relationships-4.md) | Optional | - | Relationships4 getRelationships() | setRelationships(Relationships4 relationships) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes11;
import com.coingecko.api.models.BaseToken;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Dex;
import com.coingecko.api.models.Included5;
import com.coingecko.api.models.QuoteToken;
import com.coingecko.api.models.Relationships4;
import java.io.IOException;

Included5 included5 = new Included5.Builder()
    .id("id0")
    .type("type0")
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
    .build();
```

