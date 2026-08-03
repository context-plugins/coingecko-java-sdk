
# Ohlcv

*This model accepts additional fields of type Object.*

## Structure

`Ohlcv`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`Data9`](../../doc/models/data-9.md) | Required | - | Data9 getData() | setData(Data9 data) |
| `Meta` | [`Meta`](../../doc/models/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes4;
import com.coingecko.api.models.Base;
import com.coingecko.api.models.Data9;
import com.coingecko.api.models.Meta;
import com.coingecko.api.models.Ohlcv;
import com.coingecko.api.models.Quote;
import java.io.IOException;
import java.util.Arrays;

Ohlcv ohlcv = new Ohlcv.Builder(
    new Data9.Builder(
        "id0",
        "type0",
        new Attributes4.Builder(
            Arrays.asList(
                Arrays.asList(
                    68.6D
                )
            )
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new Meta.Builder()
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
        .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

