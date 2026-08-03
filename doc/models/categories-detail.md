
# Categories Detail

*This model accepts additional fields of type Object.*

## Structure

`CategoriesDetail`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | Category ID | String getId() | setId(String id) |
| `Name` | `String` | Optional | Category name | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CategoriesDetail;
import java.io.IOException;

CategoriesDetail categoriesDetail = new CategoriesDetail.Builder()
    .id("id6")
    .name("name6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

