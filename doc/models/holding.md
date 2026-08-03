
# Holding

*This model accepts additional fields of type Object.*

## Structure

`Holding`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CoinId` | `String` | Required | Coin ID | String getCoinId() | setCoinId(String coinId) |
| `Amount` | [`double`](../../doc/models/precision.md) | Required | Amount of cryptocurrency held | double getAmount() | setAmount(double amount) |
| `PercentageOfTotalSupply` | [`double`](../../doc/models/precision.md) | Required | Percentage of total crypto supply | double getPercentageOfTotalSupply() | setPercentageOfTotalSupply(double percentageOfTotalSupply) |
| `AmountPerShare` | [`double`](../../doc/models/precision.md) | Required | Amount of cryptocurrency per share | double getAmountPerShare() | setAmountPerShare(double amountPerShare) |
| `EntityValueUsdPercentage` | [`double`](../../doc/models/precision.md) | Required | Percentage of entity's total treasury value | double getEntityValueUsdPercentage() | setEntityValueUsdPercentage(double entityValueUsdPercentage) |
| `CurrentValueUsd` | [`double`](../../doc/models/precision.md) | Required | Current value of holdings in USD | double getCurrentValueUsd() | setCurrentValueUsd(double currentValueUsd) |
| `TotalEntryValueUsd` | [`double`](../../doc/models/precision.md) | Required | Total entry cost in USD | double getTotalEntryValueUsd() | setTotalEntryValueUsd(double totalEntryValueUsd) |
| `AverageEntryValueUsd` | [`double`](../../doc/models/precision.md) | Required | Average entry cost per unit in USD | double getAverageEntryValueUsd() | setAverageEntryValueUsd(double averageEntryValueUsd) |
| `UnrealizedPnl` | [`double`](../../doc/models/precision.md) | Required | Unrealized profit and loss for this holding | double getUnrealizedPnl() | setUnrealizedPnl(double unrealizedPnl) |
| `HoldingAmountChange` | [`HoldingAmountChange`](../../doc/models/holding-amount-change.md) | Optional | Holding amount changes over different timeframes | HoldingAmountChange getHoldingAmountChange() | setHoldingAmountChange(HoldingAmountChange holdingAmountChange) |
| `HoldingChangePercentage` | [`HoldingChangePercentage`](../../doc/models/holding-change-percentage.md) | Optional | Holding change percentages over different timeframes | HoldingChangePercentage getHoldingChangePercentage() | setHoldingChangePercentage(HoldingChangePercentage holdingChangePercentage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Holding;
import com.coingecko.api.models.HoldingAmountChange;
import com.coingecko.api.models.HoldingChangePercentage;
import java.io.IOException;

Holding holding = new Holding.Builder(
    "coin_id8",
    237.94D,
    57.12D,
    167.9D,
    131.74D,
    60.3D,
    165.38D,
    5.6D,
    199.9D
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
.build();
```

