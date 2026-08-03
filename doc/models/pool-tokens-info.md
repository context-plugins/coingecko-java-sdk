
# Pool Tokens Info

*This model accepts additional fields of type Object.*

## Structure

`PoolTokensInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Data` | [`List<Data12>`](../../doc/models/data-12.md) | Required | - | List<Data12> getData() | setData(List<Data12> data) |
| `Included` | [`List<Included3>`](../../doc/models/included-3.md) | Optional | Included pool data, present when include=pool is specified | List<Included3> getIncluded() | setIncluded(List<Included3> included) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import com.coingecko.api.ApiHelper;
import com.coingecko.api.models.Attributes7;
import com.coingecko.api.models.Attributes8;
import com.coingecko.api.models.Data12;
import com.coingecko.api.models.Data5;
import com.coingecko.api.models.GtScoreDetails;
import com.coingecko.api.models.Holders;
import com.coingecko.api.models.Image6;
import com.coingecko.api.models.Included3;
import com.coingecko.api.models.Pool2;
import com.coingecko.api.models.PoolTokensInfo;
import com.coingecko.api.models.Relationships2;
import com.coingecko.api.models.containers.Attributes7IsHoneypot;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

PoolTokensInfo poolTokensInfo = new PoolTokensInfo.Builder(
    Arrays.asList(
        new Data12.Builder(
            "id0",
            "type0",
            new Attributes7.Builder(
                "address0",
                "name4",
                "symbol6",
                220,
                "image_url0",
                new Image6.Builder()
                    .thumb("thumb4")
                    .small("small0")
                    .large("large8")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                "banner_image_url6",
                "coingecko_coin_id4",
                Arrays.asList(
                    "websites5",
                    "websites6"
                ),
                "discord_url8",
                "farcaster_url6",
                "zora_url4",
                "telegram_handle2",
                "twitter_handle8",
                "description4",
                173.1D,
                new GtScoreDetails.Builder()
                    .pool(155.82D)
                    .transaction(141.8D)
                    .creation(88.54D)
                    .info(69.28D)
                    .holders(31.82D)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                false,
                Arrays.asList(
                    "categories8",
                    "categories7"
                ),
                Arrays.asList(
                    "gt_category_ids6",
                    "gt_category_ids7"
                ),
                new Holders.Builder()
                    .count(46)
                    .distributionPercentage(new LinkedHashMap<String, String>() {{
                        put("key0", "distribution_percentage0");
                        put("key1", "distribution_percentage1");
                    }})
                    .lastUpdated("last_updated8")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                "mint_authority6",
                "freeze_authority2",
                Attributes7IsHoneypot.fromBoolean(
                    true
                ),
                "developer_address0",
                "developer_holding_percentage2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Relationships2.Builder()
                .pool(new Pool2.Builder()
                    .data(new Data5.Builder()
                        .id("id0")
                        .type("type0")
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build())
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.included(Arrays.asList(
        new Included3.Builder()
            .id("id2")
            .type("type8")
            .attributes(new Attributes8.Builder()
                .baseTokenAddress("base_token_address4")
                .quoteTokenAddress("quote_token_address0")
                .quoteTokenAddresses(Arrays.asList(
                    "quote_token_addresses1",
                    "quote_token_addresses2",
                    "quote_token_addresses3"
                ))
                .sentimentVotePositivePercentage(60.36D)
                .sentimentVoteNegativePercentage(189.9D)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

