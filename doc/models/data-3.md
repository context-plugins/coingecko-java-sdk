
# Data 3

*This model accepts additional fields of type Object.*

## Structure

`Data3`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloorPrice` | `String` | Required | NFT collection floor price | String getFloorPrice() | setFloorPrice(String floorPrice) |
| `FloorPriceInUsd24HPercentageChange` | `String` | Required | NFT collection floor price in USD 24 hours percentage change | String getFloorPriceInUsd24HPercentageChange() | setFloorPriceInUsd24HPercentageChange(String floorPriceInUsd24HPercentageChange) |
| `H24Volume` | `String` | Required | NFT collection volume in 24 hours | String getH24Volume() | setH24Volume(String h24Volume) |
| `H24AverageSalePrice` | `String` | Required | NFT collection 24 hours average sale price | String getH24AverageSalePrice() | setH24AverageSalePrice(String h24AverageSalePrice) |
| `Sparkline` | `String` | Required | NFT collection sparkline image URL | String getSparkline() | setSparkline(String sparkline) |
| `Content` | [`Content`](../../doc/models/content.md) | Required | - | Content getContent() | setContent(Content content) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Content;
import com.coingecko.api.models.Data3;
import java.io.IOException;

Data3 data3 = new Data3.Builder(
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
.build();
```

