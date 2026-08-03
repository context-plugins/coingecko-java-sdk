
# Meta

*This model accepts additional fields of type Object.*

## Structure

`Meta`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Base` | [`Base`](../../doc/models/base.md) | Optional | Base token metadata | Base getBase() | setBase(Base base) |
| `Quote` | [`Quote`](../../doc/models/quote.md) | Optional | Quote token metadata | Quote getQuote() | setQuote(Quote quote) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Base;
import com.coingecko.api.models.Meta;
import com.coingecko.api.models.Quote;
import java.io.IOException;

Meta meta = new Meta.Builder()
    .base(new Base.Builder()
        .name("name6")
        .symbol("symbol2")
        .coingeckoCoinId("coingecko_coin_id2")
        .address("address2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .quote(new Quote.Builder()
        .name("name0")
        .symbol("symbol2")
        .coingeckoCoinId("coingecko_coin_id8")
        .address("address6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

