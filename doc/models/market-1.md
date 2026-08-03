
# Market 1

Ticker exchange

*This model accepts additional fields of type Object.*

## Structure

`Market1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | Exchange name | String getName() | setName(String name) |
| `Identifier` | `String` | Optional | Exchange identifier | String getIdentifier() | setIdentifier(String identifier) |
| `HasTradingIncentive` | `Boolean` | Optional | Exchange trading incentive | Boolean getHasTradingIncentive() | setHasTradingIncentive(Boolean hasTradingIncentive) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Market1;
import java.io.IOException;

Market1 market1 = new Market1.Builder()
    .name("name6")
    .identifier("identifier6")
    .hasTradingIncentive(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

