
# Launchpad Details

Launchpad details for pump-style tokens

*This model accepts additional fields of type Object.*

## Structure

`LaunchpadDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GraduationPercentage` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getGraduationPercentage() | setGraduationPercentage(Double graduationPercentage) |
| `Completed` | `Boolean` | Optional | - | Boolean getCompleted() | setCompleted(Boolean completed) |
| `CompletedAt` | `String` | Optional | - | String getCompletedAt() | setCompletedAt(String completedAt) |
| `MigratedDestinationPoolAddress` | `String` | Optional | - | String getMigratedDestinationPoolAddress() | setMigratedDestinationPoolAddress(String migratedDestinationPoolAddress) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.LaunchpadDetails;
import java.io.IOException;

LaunchpadDetails launchpadDetails = new LaunchpadDetails.Builder()
    .graduationPercentage(117.62D)
    .completed(false)
    .completedAt("completed_at4")
    .migratedDestinationPoolAddress("migrated_destination_pool_address8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

