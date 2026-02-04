# Enrichment Waterfall (Company Intelligence)

A lightweight n8n workflow that enriches a company from a single input name using a **waterfall strategy**:
**Apollo → Google (SerpAPI) → BrasilAPI**.

It normalizes the input, applies fallback searches, selects the best organization match, and returns a structured dataset with company identity (domain/website/LinkedIn/industries) plus official registry data (CNPJ, legal name, CNAE, address).

## Run
Import the workflow JSON into n8n, set your API keys as environment variables, and call the webhook with:
```json
{ "companies": ["your company name"] }
