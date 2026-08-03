
# Transaction

*This model accepts additional fields of type Object.*

## Structure

`Transaction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Date` | [`double`](../../doc/models/precision.md) | Required | Transaction date in UNIX timestamp | double getDate() | setDate(double date) |
| `SourceUrl` | `String` | Required | Source document URL | String getSourceUrl() | setSourceUrl(String sourceUrl) |
| `CoinId` | `String` | Required | Coin ID | String getCoinId() | setCoinId(String coinId) |
| `Type` | [`Type`](../../doc/models/type.md) | Required | Transaction type | Type getType() | setType(Type type) |
| `HoldingNetChange` | [`double`](../../doc/models/precision.md) | Required | Net change in holdings after the transaction | double getHoldingNetChange() | setHoldingNetChange(double holdingNetChange) |
| `TransactionValueUsd` | [`double`](../../doc/models/precision.md) | Required | Transaction value in USD | double getTransactionValueUsd() | setTransactionValueUsd(double transactionValueUsd) |
| `HoldingBalance` | [`double`](../../doc/models/precision.md) | Required | Total holding balance after the transaction | double getHoldingBalance() | setHoldingBalance(double holdingBalance) |
| `AverageEntryValueUsd` | [`double`](../../doc/models/precision.md) | Required | Average entry value in USD after the transaction | double getAverageEntryValueUsd() | setAverageEntryValueUsd(double averageEntryValueUsd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Transaction;
import com.coingecko.api.models.Type;
import java.io.IOException;

Transaction transaction = new Transaction.Builder(
    74.66D,
    "source_url6",
    "coin_id4",
    Type.BUY,
    170.58D,
    77.64D,
    20.1D,
    85.04D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

