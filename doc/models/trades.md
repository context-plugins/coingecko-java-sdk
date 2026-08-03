
# Trades

*This model accepts additional fields of type Object.*

## Structure

`Trades`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Data8>`](../../doc/models/data-8.md) | Required | - | List<Data8> getData() | setData(List<Data8> data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes3;
import com.coingecko.api.models.Data8;
import com.coingecko.api.models.Trades;
import java.io.IOException;
import java.util.Arrays;

Trades trades = new Trades.Builder(
    Arrays.asList(
        new Data8.Builder(
            "id0",
            "type0",
            new Attributes3.Builder(
                184,
                "tx_hash2",
                "tx_from_address4",
                "from_token_amount6",
                "to_token_amount0",
                "price_from_in_currency_token0",
                "price_to_in_currency_token8",
                "price_from_in_usd4",
                "price_to_in_usd8",
                "block_timestamp4",
                "kind2",
                "volume_in_usd2",
                "from_token_address8",
                "to_token_address8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

