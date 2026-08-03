
# Ath Date

NFT collection all time highs date

*This model accepts additional fields of type Object.*

## Structure

`AthDate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NativeCurrency` | `LocalDateTime` | Optional | - | LocalDateTime getNativeCurrency() | setNativeCurrency(LocalDateTime nativeCurrency) |
| `Usd` | `LocalDateTime` | Optional | - | LocalDateTime getUsd() | setUsd(LocalDateTime usd) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.DateTimeHelper;
import com.coingecko.api.models.AthDate;
import java.io.IOException;

AthDate athDate = new AthDate.Builder()
    .nativeCurrency(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .usd(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

