# AI pricing dataset

API list prices for AI models and GPU cloud rental, as CSV. Each row links the vendor page the price was read from and the page on [aiblogly.com](https://www.aiblogly.com) that tracks it.

Snapshot: 24 November 2026 (embeddings: Cohere and Mistral added 27 November). Prices change without notice; check the vendor page before relying on a figure. The live versions are updated on aiblogly.com.

| File | Rows | What it holds | Live page |
|---|---|---|---|
| `data/llm-api-pricing.csv` | 260 | Language models: input and output price per 1M tokens, context window, release date | [AI token cost calculator](https://www.aiblogly.com/ai-token-cost-calculator) |
| `data/media-api-pricing.csv` | 148 | Image, video and audio generation models, price as the vendor lists it | [Video API pricing](https://www.aiblogly.com/ai-video-generation-api-pricing) |
| `data/gpu-cloud-pricing.csv` | 78 | GPU rental per GPU-hour, 12 providers | [GPU cloud pricing](https://www.aiblogly.com/gpu-cloud-pricing) |
| `data/speech-to-text-pricing.csv` | 24 | Transcription APIs, per minute | [Speech-to-text API pricing](https://www.aiblogly.com/speech-to-text-api-pricing) |
| `data/embedding-pricing.csv` | 17 | Embedding APIs, per 1M tokens | [Embedding API pricing](https://www.aiblogly.com/embedding-api-pricing) |

## Columns

- `pricing_as_listed` / `listed_price`: the price in the vendor's own words and unit.
- `input_usd_per_1m`, `output_usd_per_1m`, `usd_per_*`: the same figure in one unit so columns sort. Conversions are plain arithmetic (an 8-GPU instance price divided by 8, per hour divided by 60).
- `vendor_source`: the vendor page the figure was read from.
- `last_verified`: the day the row was last checked against that page.

Rankings and Elo scores are not included because they change daily. They are at [aiblogly.com/benchmarks](https://www.aiblogly.com/benchmarks).

The full model list is also served as JSON at [aiblogly.com/models.json](https://www.aiblogly.com/models.json).

## Licence

CC BY 4.0. Credit "aiblogly.com" with a link to the page the data came from.
