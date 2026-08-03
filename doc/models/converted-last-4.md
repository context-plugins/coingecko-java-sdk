
# Converted Last 4

Derivative converted last price

*This model accepts additional fields of type Object.*

## Structure

`ConvertedLast4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Btc` | `String` | Optional | - | String getBtc() | setBtc(String btc) |
| `Eth` | `String` | Optional | - | String getEth() | setEth(String eth) |
| `Usd` | `String` | Optional | - | String getUsd() | setUsd(String usd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.ConvertedLast4;
import java.io.IOException;

ConvertedLast4 convertedLast4 = new ConvertedLast4.Builder()
    .btc("btc2")
    .eth("eth0")
    .usd("usd0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

