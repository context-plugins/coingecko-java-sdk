
# Categories List

*This model accepts additional fields of type Object.*

## Structure

`CategoriesList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CategoryId` | `String` | Required | Category ID | String getCategoryId() | setCategoryId(String categoryId) |
| `Name` | `String` | Required | Category name | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.CategoriesList;
import java.io.IOException;

CategoriesList categoriesList = new CategoriesList.Builder(
    "category_id0",
    "name8"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

