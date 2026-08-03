
# Nf Ts List

*This model accepts additional fields of type Object.*

## Structure

`NfTsList`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | NFT collection ID | String getId() | setId(String id) |
| `ContractAddress` | `String` | Required | NFT collection contract address | String getContractAddress() | setContractAddress(String contractAddress) |
| `Name` | `String` | Required | NFT collection name | String getName() | setName(String name) |
| `AssetPlatformId` | `String` | Required | NFT collection asset platform ID | String getAssetPlatformId() | setAssetPlatformId(String assetPlatformId) |
| `Symbol` | `String` | Required | NFT collection symbol | String getSymbol() | setSymbol(String symbol) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.NfTsList;
import java.io.IOException;

NfTsList nfTsList = new NfTsList.Builder(
    "id8",
    "contract_address2",
    "name8",
    "asset_platform_id0",
    "symbol0"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

