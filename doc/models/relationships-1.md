
# Relationships 1

*This model accepts additional fields of type Object.*

## Structure

`Relationships1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Network` | [`Network`](../../doc/models/network.md) | Optional | - | Network getNetwork() | setNetwork(Network network) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.Network;
import com.coingecko.api.models.Relationships1;
import java.io.IOException;

Relationships1 relationships1 = new Relationships1.Builder()
    .network(new Network.Builder()
        .data(new Data5.Builder()
            .id("id0")
            .type("type0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

