| **Property Name** | **Data Type** | **Details** |
|---|---|---|
| **`type`** (required) | `string` | The value of this property **must** be `openc2` |
| **`command`** (required) | `string` |  |
| **`content_b64`** (required) | `string` | An OpenC2 command that is base64 encoded (see Section 4 of [RFC 4649]). |
| **`headers`** (optional) | `dictionary` | This property contains any required HTTP headers.   The key for each entry **MUST** be a `string` that uniquely identifies this header. The value for each key **MUST** be a `list` of `string`. |
