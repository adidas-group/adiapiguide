# Adidas API Guidelines Ruleset

- all JSON fields follow `camelCase`
- field names are ASCII alphanumeric characters or `_` or `$`
- collection/array fields have names in plural
- all requests go through `https` protocol
- every API operation needs to have at least on `2xx` response
- `GET` request cannot accept a `body` parameter
- all responses are of media type `application/hal+json`
- all error responses are of media type `application/problem+json`
- every request should support `application/json` media type
- `application/hal+json` follows https://supermodel.io/adidas/api/HAL `JSON-Schema`
- `application/problem+json` messages must include `title` and `detail` fields
- `application/problem+json` messages should include `type` field
- date and time follow `ISO 8601` standard: https://www.iso.org/iso-8601-date-and-time-format.html
- language codes follow `ISO 639` standard: https://www.iso.org/iso-639-language-codes.html
- country codes follow `ISO 3166 alpha-2` standard: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2
- currency codes follow `ISO 4217` standard: https://en.wikipedia.org/wiki/ISO_4217
- `202` response code is used after creating an asynchronous process request
- a successful and finished async api request returns `303` response code and sends the target resource location in the `Link` header
- `URI` cannot contain a `-` character
- `HTTP` headers use `Hyphenated-Pascal-Case` notation
- `HTTP` headers cannot include `X-` headers (https://tools.ietf.org/html/rfc6648). All non-standard headers are named without the `X-` prefix.