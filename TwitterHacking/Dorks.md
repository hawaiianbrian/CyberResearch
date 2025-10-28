# Twitter / X Search Operators (Dorks)

Use these search operators in Twitter / X search (or the Advanced Search page) to refine results during OSINT and threat research. Always follow applicable laws and the platform's Terms of Service when conducting research.

## Basic operators

| Operator | Description | Example |
|---------:|-------------|---------|
| `<word1> <word2>` | Tweets containing both word1 AND word2 (order not required). | `malware "remote code execution"` |
| `"phrase"` | Tweets containing the exact phrase. | `"password leak"` |
| `<word1> OR <word2>` | Tweets containing word1 OR word2. | `ransomware OR "data breach"` |
| `"word1" -"word2"` | Tweets containing "word1" but **not** "word2". (Use minus to exclude.) | `"exploit" -"PoC"` |
| `from:<account>` | All tweets posted by the specified account. | `from:offsec` |
| `to:<account>` | All tweets sent to the specified account (mentions in replies). | `to:security` |
| `<word> since:YYYY-MM-DD` | Tweets containing `<word>` posted **on or after** the date. | `leak since:2023-01-01` |
| `<word> until:YYYY-MM-DD` | Tweets containing `<word>` posted **before** the date (exclusive). | `malware until:2022-12-31` |
| `lang:<code>` | Limit results to a language (ISO 639-1 codes, e.g., `en`, `es`). | `malware lang:en` |
| `-filter:retweets` | Exclude retweets from results. | `CVE-2025 -filter:retweets` |
| `filter:replies` | Include only replies. | `to:incidentresp filter:replies` |

## Extended / advanced operators

| Operator | Description | Example |
|----------|-------------|---------|
| `url:<domain>` | Tweets that include a URL containing the specified domain or substring. Useful for finding tweets linking to a site. | `url:exploit-db.com` |
| `filter:links` | Only tweets that contain at least one link. | `malware filter:links` |
| `filter:media` | Only tweets that include media (image/video/GIF). | `incident response filter:media` |
| `has:images` | Only tweets with attached images. | `geolocation has:images` |
| `has:videos` | Only tweets with native videos. | `breach has:videos` |
| `filter:videos` | Tweets containing video media specifically. | `malware filter:videos` |
| `min_faves:<number>` | Tweets with at least that many likes/favorites (good to find high-engagement posts). | `"zero-day" min_faves:100` |
| `min_retweets:<number>` | Tweets with at least that many retweets. | `CVE-2025 min_retweets:50` |
| `near:"<place>" within:<radius>` | Tweets geotagged near a location within a radius (distance units depend on the UI; try `mi` or `km`). | `cyberattack near:"Atlanta" within:10mi` |
| `place_country:<code>` | Tweets geotagged in a specific country (country code or place identifier). | `DDoS place_country:US` |

## Combining operators (examples)

- Tweets by a user about exploits since Jan 1, 2024:
