
# Exchanges List

*This model accepts additional fields of type Object.*

## Structure

`ExchangesList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Exchange ID | String getId() | setId(String id) |
| `Name` | `String` | Required | Exchange name | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ExchangesList;
import java.io.IOException;

ExchangesList exchangesList = new ExchangesList.Builder(
    "id8",
    "name8"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

