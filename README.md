# Art Institute of Chicago API 

This repository contains the full documentation and command reference for working with the [Art Institute of Chicago public API](https://api.artic.edu/api/v1), completed as part of an API testing lab using Postman and HTTPie.

---

## Repository Structure

```
├── README.md                  
├── API_ONBOARDING_REPORT.md   
├── httpie-commands.md         
├── Exitosa1.png               
├── Exitosa2.png               
├── Exitosa3.png               
├── 404.png                    
├── 400.png                   
├── 403.png                    
├── AuthCorrect.png            
└── AuthIncorrect.png          
```

---

## API Summary

| Field | Detail |
|-------|--------|
| **Name** | Art Institute of Chicago API |
| **Base URL** | `https://api.artic.edu/api/v1` |
| **Auth Type** | No authentication required (public) |
| **Rate Limit** | Not specified |
| **Docs** | https://api.artic.edu/docs |

---

## Collections Covered

### Happy Path
Requests that validate the core endpoints work correctly.

| Request | Description |
|---------|-------------|
| Run_baseUrl | Base API response |
| Run_resource | List of artworks |
| Run_id | Single artwork by ID |
| Run_query | Search by keyword |
| Run_apikey | Auth attempt (no real key needed) |

### RealRequest


| Request | Description |
|---------|-------------|
| PublicDomain | Search filtered by public domain artworks |
| ArtworkDetail | Artwork detail with specific fields |
| Image | Full image via IIIF protocol |

### Errors
Intentional error scenarios to validate API error handling.

| Request | Expected | Obtained |
|---------|----------|----------|
| 404 | 404 Not Found | 400 Bad Request |
| 400 | 400 Bad Request | 400 Bad Request |
| 401 | 401 Unauthorized | 400 Bad Request |
| 403 | 403 Forbidden | 403 Forbidden |


---

## Environment Variables

Used in both Postman and HTTPie commands:

| Variable | Value |
|----------|-------|
| `{{baseurl}}` | `https://api.artic.edu/api/v1` |
| `{{resource}}` | `artworks` |
| `{{id}}` | `129884` |
| `{{query}}` | `monet` |
| `{{apikey}}` | `N/A` |

---

## Tools Used

- **Postman** 
- **HTTPie Desktop**
- **HTTPie CLI** 

---

## Files

- [`API_ONBOARDING_REPORT.md`](API_ONBOARDING_REPORT.md) — Full onboarding report with endpoint table and screenshot evidence
- [`httpie-commands.md`](httpie-commands.md) — All equivalent HTTPie commands ready to copy and run
