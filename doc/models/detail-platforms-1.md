
# Detail Platforms 1

*This model accepts additional fields of type Object.*

## Structure

`DetailPlatforms1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DecimalPlace` | `Integer` | Optional | Token decimal place | Integer getDecimalPlace() | setDecimalPlace(Integer decimalPlace) |
| `ContractAddress` | `String` | Optional | Token contract address | String getContractAddress() | setContractAddress(String contractAddress) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.DetailPlatforms1;
import java.io.IOException;

DetailPlatforms1 detailPlatforms1 = new DetailPlatforms1.Builder()
    .decimalPlace(126)
    .contractAddress("contract_address0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

