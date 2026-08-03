
# Code Additions Deletions 4 Weeks 1

Code additions and deletions in 4 weeks

*This model accepts additional fields of type Object.*

## Structure

`CodeAdditionsDeletions4Weeks1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Additions` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getAdditions() | setAdditions(Double additions) |
| `Deletions` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getDeletions() | setDeletions(Double deletions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CodeAdditionsDeletions4Weeks1;
import java.io.IOException;

CodeAdditionsDeletions4Weeks1 codeAdditionsDeletions4Weeks1 = new CodeAdditionsDeletions4Weeks1.Builder()
    .additions(199.92D)
    .deletions(75.32D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

