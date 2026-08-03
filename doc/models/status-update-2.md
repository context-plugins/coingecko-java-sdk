
# Status Update 2

*This model accepts additional fields of type Object.*

## Structure

`StatusUpdate2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | Status update description | String getDescription() | setDescription(String description) |
| `Category` | `String` | Optional | Status update category | String getCategory() | setCategory(String category) |
| `CreatedAt` | `String` | Optional | Status update creation time | String getCreatedAt() | setCreatedAt(String createdAt) |
| `User` | `String` | Optional | Status update user | String getUser() | setUser(String user) |
| `UserTitle` | `String` | Optional | Status update user title | String getUserTitle() | setUserTitle(String userTitle) |
| `Pin` | `Boolean` | Optional | Whether status update is pinned | Boolean getPin() | setPin(Boolean pin) |
| `Project` | [`Project`](../../doc/models/project.md) | Optional | Project information | Project getProject() | setProject(Project project) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.StatusUpdate2;
import java.io.IOException;

StatusUpdate2 statusUpdate2 = new StatusUpdate2.Builder()
    .description("description2")
    .category("category0")
    .createdAt("created_at0")
    .user("user2")
    .userTitle("user_title6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

