
# Relationships 4

*This model accepts additional fields of type Object.*

## Structure

`Relationships4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BaseToken` | [`BaseToken`](../../doc/models/base-token.md) | Optional | - | BaseToken getBaseToken() | setBaseToken(BaseToken baseToken) |
| `QuoteToken` | [`QuoteToken`](../../doc/models/quote-token.md) | Optional | - | QuoteToken getQuoteToken() | setQuoteToken(QuoteToken quoteToken) |
| `Dex` | [`Dex`](../../doc/models/dex.md) | Optional | - | Dex getDex() | setDex(Dex dex) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.BaseToken;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Dex;
import com.coingecko.api.models.QuoteToken;
import com.coingecko.api.models.Relationships4;
import java.io.IOException;

Relationships4 relationships4 = new Relationships4.Builder()
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
    .build();
```

