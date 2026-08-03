
# Market

Exchange information

*This model accepts additional fields of type Object.*

## Structure

`Market`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | Exchange name | String getName() | setName(String name) |
| `Identifier` | `String` | Optional | Exchange identifier | String getIdentifier() | setIdentifier(String identifier) |
| `HasTradingIncentive` | `Boolean` | Optional | Exchange trading incentive | Boolean getHasTradingIncentive() | setHasTradingIncentive(Boolean hasTradingIncentive) |
| `Logo` | `String` | Optional | Exchange logo URL | String getLogo() | setLogo(String logo) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Market;
import java.io.IOException;

Market market = new Market.Builder()
    .name("name0")
    .identifier("identifier2")
    .hasTradingIncentive(false)
    .logo("logo6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

