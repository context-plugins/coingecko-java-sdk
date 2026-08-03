
# Base

Base token metadata

*This model accepts additional fields of type Object.*

## Structure

`Base`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Symbol` | `String` | Optional | - | String getSymbol() | setSymbol(String symbol) |
| `CoingeckoCoinId` | `String` | Optional | - | String getCoingeckoCoinId() | setCoingeckoCoinId(String coingeckoCoinId) |
| `Address` | `String` | Optional | - | String getAddress() | setAddress(String address) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Base;
import java.io.IOException;

Base base = new Base.Builder()
    .name("name6")
    .symbol("symbol2")
    .coingeckoCoinId("coingecko_coin_id2")
    .address("address2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

