
# Converted Volume 1

Ticker converted volume

*This model accepts additional fields of type Object.*

## Structure

`ConvertedVolume1`

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
import com.coingecko.api.models.ConvertedVolume1;
import java.io.IOException;

ConvertedVolume1 convertedVolume1 = new ConvertedVolume1.Builder()
    .btc(9.9D)
    .eth(50.68D)
    .usd(239.98D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

