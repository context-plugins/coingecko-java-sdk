
# Nft 1

*This model accepts additional fields of type Object.*

## Structure

`Nft1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | NFT collection ID | String getId() | setId(String id) |
| `Name` | `String` | Required | NFT collection name | String getName() | setName(String name) |
| `Symbol` | `String` | Required | NFT collection symbol | String getSymbol() | setSymbol(String symbol) |
| `Thumb` | `String` | Required | NFT collection thumb image URL | String getThumb() | setThumb(String thumb) |
| `NftContractId` | `int` | Required | NFT contract internal ID | int getNftContractId() | setNftContractId(int nftContractId) |
| `NativeCurrencySymbol` | `String` | Required | NFT collection native currency symbol | String getNativeCurrencySymbol() | setNativeCurrencySymbol(String nativeCurrencySymbol) |
| `FloorPriceInNativeCurrency` | [`double`](../../doc/models/precision.md) | Required | NFT collection floor price in native currency | double getFloorPriceInNativeCurrency() | setFloorPriceInNativeCurrency(double floorPriceInNativeCurrency) |
| `FloorPrice24HPercentageChange` | [`double`](../../doc/models/precision.md) | Required | NFT collection floor price 24 hours percentage change | double getFloorPrice24HPercentageChange() | setFloorPrice24HPercentageChange(double floorPrice24HPercentageChange) |
| `Data` | [`Data3`](../../doc/models/data-3.md) | Required | - | Data3 getData() | setData(Data3 data) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Content;
import com.coingecko.api.models.Data3;
import com.coingecko.api.models.Nft1;
import java.io.IOException;

Nft1 nft1 = new Nft1.Builder(
    "id8",
    "name8",
    "symbol0",
    "thumb6",
    162,
    "native_currency_symbol2",
    172.18D,
    199.7D,
    new Data3.Builder(
        "floor_price8",
        "floor_price_in_usd_24h_percentage_change0",
        "h24_volume8",
        "h24_average_sale_price8",
        "sparkline8",
        new Content.Builder()
            .title("title0")
            .description("description6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

