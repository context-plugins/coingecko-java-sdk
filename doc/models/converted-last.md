
# Converted Last

Converted last price

*This model accepts additional fields of type Object.*

## Structure

`ConvertedLast`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Btc` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getBtc() | setBtc(Double btc) |
| `Eth` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getEth() | setEth(Double eth) |
| `Usd` | [`Double`](../../doc/models/precision.md) | Optional | - | Double getUsd() | setUsd(Double usd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ConvertedLast;
import java.io.IOException;

ConvertedLast convertedLast = new ConvertedLast.Builder()
    .btc(150.76D)
    .eth(191.54D)
    .usd(124.84D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

