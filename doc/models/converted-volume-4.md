
# Converted Volume 4

Derivative converted volume

*This model accepts additional fields of type Object.*

## Structure

`ConvertedVolume4`

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
import com.coingecko.api.models.ConvertedVolume4;
import java.io.IOException;

ConvertedVolume4 convertedVolume4 = new ConvertedVolume4.Builder()
    .btc("btc0")
    .eth("eth8")
    .usd("usd8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

