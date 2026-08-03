
# Rates

*This model accepts additional fields of type Object.*

## Structure

`Rates`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Currency name | String getName() | setName(String name) |
| `Unit` | `String` | Required | Currency unit symbol | String getUnit() | setUnit(String unit) |
| `Value` | [`double`](../../doc/models/precision.md) | Required | Exchange rate value relative to BTC | double getValue() | setValue(double value) |
| `Type` | `String` | Required | Currency type: crypto, fiat, or commodity | String getType() | setType(String type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Rates;
import java.io.IOException;

Rates rates = new Rates.Builder(
    "name4",
    "unit2",
    198.16D,
    "type6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

