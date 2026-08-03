
# Status Update

*This model accepts additional fields of type Object.*

## Structure

`StatusUpdate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | Status update description | String getDescription() | setDescription(String description) |
| `Category` | `String` | Optional | Status update category | String getCategory() | setCategory(String category) |
| `CreatedAt` | `String` | Optional | Status update creation time | String getCreatedAt() | setCreatedAt(String createdAt) |
| `User` | `String` | Optional | Status update user | String getUser() | setUser(String user) |
| `UserTitle` | `String` | Optional | Status update user title | String getUserTitle() | setUserTitle(String userTitle) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.StatusUpdate;
import java.io.IOException;

StatusUpdate statusUpdate = new StatusUpdate.Builder()
    .description("description0")
    .category("category8")
    .createdAt("created_at8")
    .user("user0")
    .userTitle("user_title4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

