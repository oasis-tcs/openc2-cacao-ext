| **Property Name** | **Data Type** | **Details** |
|---|---|---|
| **`type`** (required) <br> | <span lang=EN style='font-family:Consolas;color:#C7254E;background:#F9F2F4'>string</span> | The value of this property **must** be <span lang=EN style='font-family:Consolas;color:#073763;background:#CFE2F3'>openc2</span> |
| **`command`** (required) | <span lang=EN style='font-family:Consolas;color:#C7254E;background:#F9F2F4'>string</span> |  |
| **`content_b64`** (required) | <span lang=EN style='font-family:Consolas;color:#C7254E;background:#F9F2F4'>string</span> | An OpenC2 command that is base64 encoded (see Section 4 of [RFC 4649]). |
| **`headers`** (optional) | <span lang=EN style='font-family:Consolas;color:#C7254E;background:#F9F2F4'>dictionary</span> | This property contains any required HTTP headers.   The key for each entry **MUST** be a `string` that uniquely identifies this header. The value for each key **MUST** be a `list` of `string`. |
