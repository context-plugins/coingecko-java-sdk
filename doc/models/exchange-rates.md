
# Exchange Rates

*This model accepts additional fields of type Object.*

## Structure

`ExchangeRates`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Rates` | [`Map<String, Rates>`](../../doc/models/rates.md) | Required | Exchange rates keyed by currency code | Map<String, Rates> getRates() | setRates(Map<String, Rates> rates) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ExchangeRates;
import com.coingecko.api.models.Rates;
import java.io.IOException;
import java.util.LinkedHashMap;

ExchangeRates exchangeRates = new ExchangeRates.Builder(
    new LinkedHashMap<String, Rates>() {{
        put("key0", new Rates.Builder(
            "name4",
            "unit2",
            198.16D,
            "type6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build());
    }}
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

