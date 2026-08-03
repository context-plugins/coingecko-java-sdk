
# Code Additions Deletions 4 Weeks

Code additions and deletions in the last 4 weeks

*This model accepts additional fields of type Object.*

## Structure

`CodeAdditionsDeletions4Weeks`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Additions` | [`Double`](../../doc/models/precision.md) | Optional | Lines added | Double getAdditions() | setAdditions(Double additions) |
| `Deletions` | [`Double`](../../doc/models/precision.md) | Optional | Lines deleted | Double getDeletions() | setDeletions(Double deletions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CodeAdditionsDeletions4Weeks;
import java.io.IOException;

CodeAdditionsDeletions4Weeks codeAdditionsDeletions4Weeks = new CodeAdditionsDeletions4Weeks.Builder()
    .additions(38.62D)
    .deletions(85.98D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

