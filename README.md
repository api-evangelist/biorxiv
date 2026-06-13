# bioRxiv

bioRxiv is a free preprint server for the biological sciences operated by Cold Spring Harbor Laboratory. It provides open access to unpublished manuscripts prior to peer review, enabling rapid dissemination of scientific findings. The platform covers all areas of biology and life sciences.

## REST API

The bioRxiv REST API (`https://api.biorxiv.org`) provides programmatic access to preprint metadata, full text links, publication status, and usage statistics for papers posted to bioRxiv and medRxiv. No authentication or API key is required.

### Key Endpoints

| Endpoint | Description |
|----------|-------------|
| `/details/{server}/{interval}/{cursor}/{format}` | Retrieve preprint metadata filtered by date range or DOI |
| `/pubs/{server}/{doi}/{cursor}/{format}` | Published preprint information |
| `/publisher/{prefix}/{interval}/{cursor}/{format}` | Articles filtered by publisher DOI prefix |
| `/funder/{ror_id}/{interval}/{cursor}/{format}` | Articles filtered by funder ROR ID |
| `/sum/{server}/{interval}/{format}` | Submission and revision count statistics |
| `/usage/{server}/{interval}/{format}` | Abstract views, full-text views, and PDF downloads |

### Response Format

All endpoints return JSON by default with two top-level keys:

- `messages` — request metadata including status, cursor, count, and total records
- `collection` — array of article objects with title, authors, DOI, date, version, license, category, abstract, and publication status

### Supported Servers

- `biorxiv` — biology preprints
- `medrxiv` — health sciences preprints

### Output Formats

- `json` (default)
- `xml` (OAI-PMH)
- `html`
- `csv`

## Access

- **Authentication**: None required
- **Rate Limits**: Not formally documented; responsible use expected
- **Cost**: Free
- **License**: Preprint content available under CC0, CC BY, CC BY-NC-ND, or other open licenses depending on the paper

## Links

- Website: https://www.biorxiv.org/
- API Base URL: https://api.biorxiv.org/
- About: https://www.biorxiv.org/about-biorxiv

## APIs.json

This repository contains an [APIs.json 0.19](https://apisjson.org/) profile for bioRxiv maintained by [API Evangelist](https://apievangelist.com/).
