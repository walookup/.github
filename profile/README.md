## WA Lookup

**Real-time WhatsApp registration, avatar and Business-account checks.**

Submit one phone number and get the WhatsApp registration result in the same HTTP response — no task queue, no polling, no callbacks. Up to 100 numbers per synchronous request. Whole lists go through the asynchronous bulk API instead.

[**Website**](https://walookup.com) · [**API documentation**](https://walookup.com/api-docs) · [**Pricing**](https://walookup.com/pricing) · [**Get an API key**](https://walookup.com/register)

### Official API example repositories

| Repository | Shape | Product code | Contents |
|---|---|---|---|
| **[WhatsApp Registration Check](https://github.com/walookup/whatsapp-number-checker-api)** | Realtime | `ws` | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[WhatsApp Avatar Check](https://github.com/walookup/whatsapp-avatar-checker-api)** | Realtime | `ws_avatar` | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[WhatsApp Business Account Check](https://github.com/walookup/whatsapp-business-checker-api)** | Realtime | `ws_business` | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[WhatsApp bulk tasks](https://github.com/walookup/whatsapp-bulk-checker-api)** | Bulk (async) | 4 products | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| [walookup-resources](https://github.com/walookup/walookup-resources) | — | — | Technical notes, guides and announcements |

Every example repository carries a machine-readable `product.json`, an `llms.txt` summary for AI clients, an OpenAPI 3.0 contract, and runnable examples in Python, Node.js, Go, Java, C#, PHP and Shell. All request paths, response fields and limits are taken from the live product pages and the published API documentation.

### Realtime or bulk?

A **realtime** check (`POST /api/v1/check`, or `POST /api/v1/batch-check` for up to 100 identifiers) answers inside the same HTTP response — that is the shape for a signup form, a checkout step or a live lookup. A **bulk task** (`POST /api/v1/bulk-tasks`) takes a `.txt`/`.csv` file of 1,000–100,000 entries, returns a task id immediately, and produces a downloadable result file — that is the shape for list cleaning, campaign preparation and enrichment runs. The two are separate endpoints and are not interchangeable.

### One key, one balance

Every product on WA Lookup uses the same API key, the same `X-API-Key` header and the same `code` / `msg` / `data` envelope, and draws from the same account balance.

### Responsible use

Results are **point-in-time signals**: they describe what a provider reported at the moment of the check. They are not identity verification, not proof of ownership, and not permission to contact anyone. Use the API only for identifiers you are authorized to process, and comply with applicable privacy laws and platform terms. Third-party trademarks belong to their respective owners; no affiliation or endorsement is implied.
