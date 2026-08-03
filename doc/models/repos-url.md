
# Repos Url

Repository URL

*This model accepts additional fields of type Object.*

## Structure

`ReposUrl`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Github` | `List<String>` | Optional | GitHub repository URL | List<String> getGithub() | setGithub(List<String> github) |
| `Bitbucket` | `List<String>` | Optional | Bitbucket repository URL | List<String> getBitbucket() | setBitbucket(List<String> bitbucket) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ReposUrl;
import java.io.IOException;
import java.util.Arrays;

ReposUrl reposUrl = new ReposUrl.Builder()
    .github(Arrays.asList(
        "github3",
        "github4"
    ))
    .bitbucket(Arrays.asList(
        "bitbucket1"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

