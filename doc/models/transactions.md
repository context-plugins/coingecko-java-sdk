
# Transactions

Transaction counts over various timeframes

*This model accepts additional fields of type Object.*

## Structure

`Transactions`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `M5` | [`M5`](../../doc/models/m5.md) | Optional | - | M5 getM5() | setM5(M5 m5) |
| `M15` | [`M5`](../../doc/models/m5.md) | Optional | - | M5 getM15() | setM15(M5 m15) |
| `M30` | [`M5`](../../doc/models/m5.md) | Optional | - | M5 getM30() | setM30(M5 m30) |
| `H1` | [`H1`](../../doc/models/h1.md) | Optional | - | H1 getH1() | setH1(H1 h1) |
| `H6` | [`H1`](../../doc/models/h1.md) | Optional | - | H1 getH6() | setH6(H1 h6) |
| `H24` | [`H1`](../../doc/models/h1.md) | Optional | - | H1 getH24() | setH24(H1 h24) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.H1;
import com.coingecko.api.models.M5;
import com.coingecko.api.models.Transactions;
import java.io.IOException;

Transactions transactions = new Transactions.Builder()
    .m5(new M5.Builder()
        .buys(154)
        .sells(38)
        .buyers(224)
        .sellers(100)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .m15(new M5.Builder()
        .buys(240)
        .sells(100)
        .buyers(106)
        .sellers(38)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .m30(new M5.Builder()
        .buys(172)
        .sells(32)
        .buyers(38)
        .sellers(226)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .h1(new H1.Builder()
        .buys(216)
        .sells(76)
        .buyers(82)
        .sellers(14)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .h6(new H1.Builder()
        .buys(32)
        .sells(148)
        .buyers(154)
        .sellers(170)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

