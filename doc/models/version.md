
# Version

Token list version

*This model accepts additional fields of type Object.*

## Structure

`Version`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Major` | [`Double`](../../doc/models/precision.md) | Optional | Major version | Double getMajor() | setMajor(Double major) |
| `Minor` | [`Double`](../../doc/models/precision.md) | Optional | Minor version | Double getMinor() | setMinor(Double minor) |
| `Patch` | [`Double`](../../doc/models/precision.md) | Optional | Patch version | Double getPatch() | setPatch(Double patch) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Version;
import java.io.IOException;

Version version = new Version.Builder()
    .major(131.98D)
    .minor(74.22D)
    .patch(252.26D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

