[Dribbble Designer Scraper](https://apify.com/heliostech/dribbble-designer-scraper?fpr=data)

# Dribbble Designer Scraper

Extract designer profiles from [Dribbble.com](https://dribbble.com) — the world's leading community for designers. Use this actor to build targeted lead lists, recruit freelance talent, or research design agencies.

## What it extracts

| Field | Description |
| --- | --- |
| `name` | Designer or studio name |
| `username` | Dribbble username |
| `location` | City and country |
| `isPro` | Whether the designer has a PRO account |
| `isAvailableForWork` | Whether the designer is open to new projects |
| `budget` | Starting project budget (e.g. "From $500/project") |
| `responseTime` | How quickly they typically respond |
| `servicesCount` | Number of services offered |
| `bio` | Profile bio/description |
| `followersCount` | Number of Dribbble followers |
| `followingCount` | Number of accounts they follow |
| `shotsCount` | Total published shots/designs |
| `skills` | Design skill tags (e.g. UI, Branding, Illustration) |
| `profileUrl` | Link to their Dribbble profile |
| `avatarUrl` | Profile photo URL |
| `websiteUrl` | Personal or studio website |
| `twitterUrl` | Twitter/X profile link |
| `scrapedAt` | Timestamp of when data was extracted |

## Use cases

- **Freelancer hiring** — Find available designers by skill and location
- **Agency prospecting** — Build outreach lists for design studios
- **Competitor research** — Analyze how designers in your niche position themselves
- **Talent databases** — Build a searchable directory of design talent
- **Market research** — Understand pricing, skills, and availability in design markets

## Input configuration

```
{
  "searchQuery": "logo designer",
  "location": "New York",
  "availability": "freelance",
  "maxResults": 200,
  "scrapeProfileDetails": true,
  "proxyConfiguration": {
    "useApifyProxy": true,
    "apifyProxyGroups": ["RESIDENTIAL"]
  }
}
```

### Input fields

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `searchQuery` | String | — | Keyword search (e.g. "UI UX", "branding", "motion") |
| `location` | String | — | Filter by city or country |
| `availability` | String | — | `freelance`, `fulltime`, `available`, or empty for all |
| `startUrls` | Array | — | Custom Dribbble URLs to start from (overrides searchQuery) |
| `maxResults` | Integer | 100 | Max profiles to extract (up to 10,000) |
| `scrapeProfileDetails` | Boolean | true | Visit each profile for full data (bio, followers, skills) |
| `proxyConfiguration` | Object | Residential | Proxy settings |

## Sample output

```
{
  "name": "Jane Studio",
  "username": "janestudio",
  "location": "New York City, NY",
  "isPro": true,
  "isAvailableForWork": true,
  "budget": "From $1,500/project",
  "responseTime": "Responds within a few hours",
  "servicesCount": 12,
  "bio": "Award-winning branding studio specializing in identity design.",
  "followersCount": "4.2K",
  "followingCount": "512",
  "shotsCount": "248",
  "skills": ["Branding", "Logo Design", "Typography", "UI/UX"],
  "profileUrl": "https://dribbble.com/janestudio",
  "avatarUrl": "https://cdn.dribbble.com/users/.../avatar.jpg",
  "websiteUrl": "https://janestudio.com",
  "twitterUrl": "https://twitter.com/janestudio",
  "scrapedAt": "2026-04-10T22:00:00.000Z"
}
```

## Pricing

This actor uses **Pay-per-result** pricing at **$3.00 per 1,000 results**.

Extracting 1,000 designer profiles costs $3.00.

## Notes

- Residential proxies are recommended to avoid rate limiting
- Enable `scrapeProfileDetails` for the most complete data set
- Dribbble requires login to view some fields — publicly accessible data only is extracted