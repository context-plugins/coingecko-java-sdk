
# Gt Score Details

GeckoTerminal trust score breakdown

*This model accepts additional fields of type Object.*

## Structure

`GtScoreDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pool` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getPool() | setPool(Double pool) |
| `Transaction` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getTransaction() | setTransaction(Double transaction) |
| `Creation` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getCreation() | setCreation(Double creation) |
| `Info` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getInfo() | setInfo(Double info) |
| `Holders` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getHolders() | setHolders(Double holders) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.GtScoreDetails;
import java.io.IOException;

GtScoreDetails gtScoreDetails = new GtScoreDetails.Builder()
    .pool(212D)
    .transaction(58.02D)
    .creation(144.72D)
    .info(125.46D)
    .holders(168D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

