
# Included 3

*This model accepts additional fields of type Object.*

## Structure

`Included3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Optional | - | String getId() | setId(String id) |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `Attributes` | [`Attributes8`](../../doc/models/attributes-8.md) | Optional | - | Attributes8 getAttributes() | setAttributes(Attributes8 attributes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes8;
import com.coingecko.api.models.Included3;
import java.io.IOException;
import java.util.Arrays;

Included3 included3 = new Included3.Builder()
    .id("id8")
    .type("type8")
    .attributes(new Attributes8.Builder()
        .baseTokenAddress("base_token_address4")
        .quoteTokenAddress("quote_token_address0")
        .quoteTokenAddresses(Arrays.asList(
            "quote_token_addresses1",
            "quote_token_addresses2",
            "quote_token_addresses3"
        ))
        .sentimentVotePositivePercentage(60.36D)
        .sentimentVoteNegativePercentage(189.9D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

