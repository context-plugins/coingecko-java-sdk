
# Converted Last 1

Ticker converted last price

*This model accepts additional fields of type Object.*

## Structure

`ConvertedLast1`

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
import com.coingecko.api.models.ConvertedLast1;
import java.io.IOException;

ConvertedLast1 convertedLast1 = new ConvertedLast1.Builder()
    .btc(118.18D)
    .eth(158.96D)
    .usd(92.26D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

