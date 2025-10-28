# Google Dorks / Search Operators

A compact, copy-and-paste ready reference of Google search operators (dorks) useful for OSINT, red team reconnaissance, vulnerability discovery and investigative research. Use responsibly and legally — do not use these techniques for unauthorized access, scanning, or data theft.

## Operators (operator → description → example)

- `site:`  
  Returns results only from the specified site or domain.  
  Example: `site:example.com`  

- `inurl:`  
  Finds pages with the term in the URL. Useful to locate login pages, admin panels, or parameters.  
  Example: `inurl:admin`  

- `allinurl:`  
  Returns results whose URLs contain **all** the specified terms.  
  Example: `allinurl: admin login`  

- `intitle:`  
  Finds pages with the term in the page title.  
  Example: `intitle:"index of"`  

- `allintitle:`  
  Returns results whose titles contain **all** the specified words.  
  Example: `allintitle: confidential report`  

- `intext:`  
  Finds pages that contain the given term in the body text.  
  Example: `intext:"password"`  

- `allintext:`  
  Returns pages that contain all specified words somewhere in the text.  
  Example: `allintext: username password "connection string"`  

- `inanchor:`  
  Finds pages where the specified text appears in anchor/link text.  
  Example: `inanchor:"download"`  

- `filetype:`  
  Restrict results to a specific file type/extension.  
  Example: `filetype:pdf "password"`  

- `OR`  
  Logical OR between terms (must be uppercase).  
  Example: `ransomware OR "data breach"`  

- `-` (minus)  
  Excludes results containing the term that follows `-`.  
  Example: `exploit -PoC`  

- `"` (quotes)  
  Search for an exact phrase.  
  Example: `"remote code execution"`  

- `*` (wildcard)  
  Acts as a placeholder for unknown words in a phrase.  
  Example: `"how to * a router"`  

- `AROUND(n)`  
  Proximity search — find results where two terms appear within *n* words of each other.  
  Example: `"sql injection" AROUND(5) "payload"`  

- `cache:`  
  Show Google's cached copy of a page (if available).  
  Example: `cache:example.com/somepage`  

- `link:`  
  Show pages that link to the specified URL. (Note: results can be incomplete.)  
  Example: `link:example.com`  

- `related:`  
  Find pages similar to the specified URL.  
  Example: `related:example.com`  

- `info:`  
  Show information that Google has about a URL (cache, similar pages, etc.).  
  Example: `info:example.com`  

- `define:`  
  Show definitions (from Google’s sources) for the given term or phrase.  
  Example: `define:phishing`  

- `before:` / `after:`  
  Restrict results to pages indexed before/after a date (YYYY-MM-DD). Useful for timeline research.  
  Example: `malware after:2024-01-01 before:2024-12-31`  

- `daterange:` *(advanced / legacy — uses Julian dates and is rarely required; prefer `before:` / `after:`)*

- `min_faves:` / `min_retweets:` *(these are Twitter-specific; not for Google search — ignore for Google dorks)*

- `near:"<place>" within:<radius>` *(geo searches are limited in Google; many results won't be geotagged — better for platform-specific searches)*

## Practical compound examples

- Find publicly indexed Excel files on a domain:
