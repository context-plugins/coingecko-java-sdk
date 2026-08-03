
# Derivatives Exchanges List

*This model accepts additional fields of type Object.*

## Structure

`DerivativesExchangesList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | Derivatives exchange ID | String getId() | setId(String id) |
| `Name` | `String` | Required | Derivatives exchange name | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DerivativesExchangesList;
import java.io.IOException;

DerivativesExchangesList derivativesExchangesList = new DerivativesExchangesList.Builder(
    "id6",
    "name6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

