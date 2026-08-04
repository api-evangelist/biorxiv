# bioRxiv

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
