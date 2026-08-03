
# Converted Volume

Converted trading volume

*This model accepts additional fields of type Object.*

## Structure

`ConvertedVolume`

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
import com.coingecko.api.models.ConvertedVolume;
import java.io.IOException;

ConvertedVolume convertedVolume = new ConvertedVolume.Builder()
    .btc(171.94D)
    .eth(212.72D)
    .usd(146.02D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

