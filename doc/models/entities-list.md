
# Entities List

*This model accepts additional fields of type Object.*

## Structure

`EntitiesList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Entity ID | String getId() | setId(String id) |
| `Symbol` | `String` | Required | Ticker symbol of public company | String getSymbol() | setSymbol(String symbol) |
| `Name` | `String` | Required | Entity name | String getName() | setName(String name) |
| `Country` | `String` | Required | Country code | String getCountry() | setCountry(String country) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.EntitiesList;
import java.io.IOException;

EntitiesList entitiesList = new EntitiesList.Builder(
    "id4",
    "symbol4",
    "name4",
    "country8"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

