
# Public Treasury Entity

*This model accepts additional fields of type Object.*

## Structure

`PublicTreasuryEntity`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | Entity name | String getName() | setName(String name) |
| `Id` | `String` | Required | Entity ID | String getId() | setId(String id) |
| `Type` | `String` | Required | Entity type: company or government | String getType() | setType(String type) |
| `Symbol` | `String` | Required | Stock market ticker symbol | String getSymbol() | setSymbol(String symbol) |
| `Country` | `String` | Required | Country code | String getCountry() | setCountry(String country) |
| `WebsiteUrl` | `String` | Required | Official website URL | String getWebsiteUrl() | setWebsiteUrl(String websiteUrl) |
| `TwitterScreenName` | `String` | Required | Official Twitter handle | String getTwitterScreenName() | setTwitterScreenName(String twitterScreenName) |
| `TotalTreasuryValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total current value of all holdings in USD | double getTotalTreasuryValueUsd() | setTotalTreasuryValueUsd(double totalTreasuryValueUsd) |
| `UnrealizedPnl` | [`double`](../../doc/models/precision.md) | Required | Unrealized profit and loss (current value minus total entry value) | double getUnrealizedPnl() | setUnrealizedPnl(double unrealizedPnl) |
| `MNav` | [`double`](../../doc/models/precision.md) | Required | Market to net asset value ratio | double getMNav() | setMNav(double mNav) |
| `TotalAssetValuePerShareUsd` | [`double`](../../doc/models/precision.md) | Required | Total asset value per share in USD | double getTotalAssetValuePerShareUsd() | setTotalAssetValuePerShareUsd(double totalAssetValuePerShareUsd) |
| `Holdings` | [`List<Holding>`](../../doc/models/holding.md) | Required | List of cryptocurrency assets held by the entity | List<Holding> getHoldings() | setHoldings(List<Holding> holdings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Holding;
import com.coingecko.api.models.HoldingAmountChange;
import com.coingecko.api.models.HoldingChangePercentage;
import com.coingecko.api.models.PublicTreasuryEntity;
import java.io.IOException;
import java.util.Arrays;

PublicTreasuryEntity publicTreasuryEntity = new PublicTreasuryEntity.Builder(
    "name6",
    "id6",
    "type4",
    "symbol8",
    "country0",
    "website_url4",
    "twitter_screen_name8",
    241.94D,
    72.54D,
    126.4D,
    252.54D,
    Arrays.asList(
        new Holding.Builder(
            "coin_id2",
            230.38D,
            49.56D,
            160.34D,
            124.18D,
            52.74D,
            157.82D,
            242.84D,
            192.34D
        )
        .holdingAmountChange(new HoldingAmountChange.Builder()
                .m7D(136.38D)
                .m14D(197.9D)
                .m30D(160.12D)
                .m90D(188.62D)
                .m1Y(142.24D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .holdingChangePercentage(new HoldingChangePercentage.Builder()
                .m7D(88.66D)
                .m14D(150.18D)
                .m30D(112.4D)
                .m90D(19.66D)
                .m1Y(94.52D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

