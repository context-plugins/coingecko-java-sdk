
# Public Treasury Transaction History

*This model accepts additional fields of type Object.*

## Structure

`PublicTreasuryTransactionHistory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Transactions` | [`List<Transaction>`](../../doc/models/transaction.md) | Required | - | List<Transaction> getTransactions() | setTransactions(List<Transaction> transactions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.PublicTreasuryTransactionHistory;
import com.coingecko.api.models.Transaction;
import com.coingecko.api.models.Type;
import java.io.IOException;
import java.util.Arrays;

PublicTreasuryTransactionHistory publicTreasuryTransactionHistory = new PublicTreasuryTransactionHistory.Builder(
    Arrays.asList(
        new Transaction.Builder(
            179.84D,
            "source_url4",
            "coin_id4",
            Type.BUY,
            83.92D,
            76.14D,
            18.6D,
            169.46D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

