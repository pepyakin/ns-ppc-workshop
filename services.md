# Curated services

A subset of the [live MPP catalog](https://mpp.dev/services) (91 services), grouped by what they're useful for. Each entry shows the base URL you POST to with `tempo request` and a docs link. Run `tempo wallet -t services <id>` to inspect endpoints.

## LLMs

- `anthropic` — Claude (Sonnet, Opus, Haiku); native + OpenAI-compat. [`anthropic.mpp.tempo.xyz`](https://anthropic.mpp.tempo.xyz) · [docs](https://docs.anthropic.com)
- `openai` — GPT, embeddings, DALL-E, Whisper, TTS. [`openai.mpp.tempo.xyz`](https://openai.mpp.tempo.xyz) · [docs](https://platform.openai.com/docs)
- `gemini` — Google Gemini text, Veo video, Nano Banana image. [`gemini.mpp.tempo.xyz`](https://gemini.mpp.tempo.xyz) · [docs](https://ai.google.dev/docs)
- `openrouter` — Unified API for 100+ LLMs, live per-model pricing. [`openrouter.mpp.tempo.xyz`](https://openrouter.mpp.tempo.xyz) · [docs](https://openrouter.ai/docs)
- `grok` — xAI: chat, web/X search, code exec, image gen, TTS. [`grok.mpp.paywithlocus.com`](https://grok.mpp.paywithlocus.com) · [docs](https://docs.x.ai)
- `groq` — Ultra-fast Llama, DeepSeek R1, Gemma, Qwen, Whisper, TTS. [`groq.mpp.paywithlocus.com`](https://groq.mpp.paywithlocus.com) · [docs](https://console.groq.com/docs)
- `mistral` — Mistral Large/Medium/Small/Codestral, Magistral, Pixtral, embeddings. [`mistral.mpp.paywithlocus.com`](https://mistral.mpp.paywithlocus.com) · [docs](https://docs.mistral.ai)
- `deepseek` — DeepSeek-V3 (chat/code) + R1 (chain-of-thought reasoning); OpenAI-compat. [`deepseek.mpp.paywithlocus.com`](https://deepseek.mpp.paywithlocus.com) · [docs](https://api-docs.deepseek.com)

## Web search & research

- `exa` — AI-powered web search, content retrieval, answers. [`exa.mpp.tempo.xyz`](https://exa.mpp.tempo.xyz) · [docs](https://docs.exa.ai)
- `tavily` — AI-optimized search, extraction, site mapping, crawling. [`tavily.mpp.paywithlocus.com`](https://tavily.mpp.paywithlocus.com) · [docs](https://docs.tavily.com)
- `perplexity` — Sonar chat with real-time web grounding, search, embeddings. [`perplexity.mpp.paywithlocus.com`](https://perplexity.mpp.paywithlocus.com) · [docs](https://docs.perplexity.ai)
- `brave` — Independent web/news/image/video search; privacy-first. [`brave.mpp.paywithlocus.com`](https://brave.mpp.paywithlocus.com) · [docs](https://api.search.brave.com/app/#/documentation)
- `parallel` — Search, page extraction, multi-hop research. [`parallelmpp.dev`](https://parallelmpp.dev) · [docs](https://parallelmpp.dev/#agents)
- `firecrawl` — Scrape, crawl, structured extraction for LLMs. [`firecrawl.mpp.tempo.xyz`](https://firecrawl.mpp.tempo.xyz) · [docs](https://docs.firecrawl.dev)
- `oxylabs` — Geo-targeted scraping (country/state/city) with JS rendering. [`oxylabs.mpp.tempo.xyz`](https://oxylabs.mpp.tempo.xyz) · [docs](https://developers.oxylabs.io/scraper-apis/web-scraper-api)
- `diffbot` — Article / product / discussion / image / video extraction. [`diffbot.mpp.paywithlocus.com`](https://diffbot.mpp.paywithlocus.com) · [docs](https://docs.diffbot.com)

## People & company enrichment

- `apollo` — Lead search + people/company enrichment (275M+ contacts). [`apollo.mpp.paywithlocus.com`](https://apollo.mpp.paywithlocus.com) · [docs](https://docs.apollo.io)
- `hunter` — Email finding, verification, company enrichment. [`hunter.mpp.paywithlocus.com`](https://hunter.mpp.paywithlocus.com) · [docs](https://hunter.io/api-documentation/v2)
- `clado` — LinkedIn deep search, people enrichment, lead research. [`clado.mpp.paywithlocus.com`](https://clado.mpp.paywithlocus.com) · [docs](https://docs.clado.ai)
- `stableenrich` — Bundled people / company / web / places / social enrichment. [`stableenrich.dev`](https://stableenrich.dev) · [docs](https://stableenrich.dev)
- `builtwith` — Tech-stack profiling across 100M+ websites. [`builtwith.mpp.paywithlocus.com`](https://builtwith.mpp.paywithlocus.com) · [docs](https://api.builtwith.com)
- `diffbot-kg` — 10B+ entity knowledge graph, company/person enrichment. [`diffbot-kg.mpp.paywithlocus.com`](https://diffbot-kg.mpp.paywithlocus.com) · [docs](https://docs.diffbot.com/reference/knowledge-graph)
- `diffbot-nl` — NLP — NER, sentiment, facts, summarization. [`diffbot-nl.mpp.paywithlocus.com`](https://diffbot-nl.mpp.paywithlocus.com) · [docs](https://docs.diffbot.com/reference/natural-language)

## Image / video / audio generation

- `suno` — Full songs + lyrics (best for the weather song). [`suno.mpp.paywithlocus.com`](https://suno.mpp.paywithlocus.com) · [docs](https://docs.sunoapi.org)
- `fal` — fal.ai: 600+ models (Flux, SD, Recraft, Grok). [`fal.mpp.tempo.xyz`](https://fal.mpp.tempo.xyz) · [docs](https://fal.ai/docs)
- `stablestudio` — Bundled image/video gen — Nano Banana, GPT Image, Grok, Flux, Sora, Veo, Seedance, Wan. [`stablestudio.dev`](https://stablestudio.dev) · [docs](https://stablestudio.dev)
- `stability-ai` — Text-to-image, edit, upscale, 3D, audio. [`stability-ai.mpp.paywithlocus.com`](https://stability-ai.mpp.paywithlocus.com) · [docs](https://platform.stability.ai/docs/api-reference)
- `replicate` — 1000s of open-source models — image, LLM, speech, video. [`replicate.mpp.paywithlocus.com`](https://replicate.mpp.paywithlocus.com) · [docs](https://replicate.com/docs/reference/http)
- `deepgram` — Nova-3 speech-to-text + Aura-2 TTS + sentiment/intent analysis. [`deepgram.mpp.paywithlocus.com`](https://deepgram.mpp.paywithlocus.com) · [docs](https://developers.deepgram.com/reference/deepgram-api-overview)

## Weather / location / mapping

- `openweather` — Current, 5-day, hourly, AQI, alerts, One Call 3.0 (best for forecast). [`openweather.mpp.paywithlocus.com`](https://openweather.mpp.paywithlocus.com) · [docs](https://openweathermap.org/api)
- `googlemaps` — Geocoding, directions, places, routes, tiles, weather, AQI, solar, pollen. [`googlemaps.mpp.tempo.xyz`](https://googlemaps.mpp.tempo.xyz) · [docs](https://developers.google.com/maps)
- `mapbox` — Geocoding, directions, isochrones, matrix, map matching, static maps. [`mapbox.mpp.paywithlocus.com`](https://mapbox.mpp.paywithlocus.com) · [docs](https://docs.mapbox.com/api/)

## Data / knowledge

- `wolframalpha` — Computational knowledge — math, science, geography, finance, nutrition. [`wolframalpha.mpp.paywithlocus.com`](https://wolframalpha.mpp.paywithlocus.com) · [docs](https://products.wolframalpha.com/api)
- `tako` — Datasets, charts, AI-built research reports. [`tako.com`](https://tako.com) · [docs](https://tako.com)
- `govlaws` — US federal regulations + change tracking, with provenance. [`govlaws.ai`](https://govlaws.ai) · [docs](https://govlaws.ai/mpp)
- `edgar` — SEC EDGAR — filings history + XBRL financial facts (no API key). [`edgar.mpp.paywithlocus.com`](https://edgar.mpp.paywithlocus.com) · [docs](https://www.sec.gov/developer)
- `edgar-search` — Full-text search across all SEC filings (10-K, 10-Q, 8-K, proxies). [`edgar-search.mpp.paywithlocus.com`](https://edgar-search.mpp.paywithlocus.com) · [docs](https://efts.sec.gov/LATEST/search-index)
- `coingecko` — Crypto prices, charts, market cap, exchanges, trending, NFTs, derivatives. [`coingecko.mpp.paywithlocus.com`](https://coingecko.mpp.paywithlocus.com) · [docs](https://docs.coingecko.com)
- `alphavantage` — Stocks, forex, crypto, commodities, indicators, news sentiment. [`alphavantage.mpp.paywithlocus.com`](https://alphavantage.mpp.paywithlocus.com) · [docs](https://www.alphavantage.co/documentation/)
- `kicksdb` — Sneaker / streetwear prices + sales history (StockX, GOAT). [`kicksdb.mpp.tempo.xyz`](https://kicksdb.mpp.tempo.xyz) · [docs](https://kicks.dev)

## Onchain

- `allium` — Onchain finance system of record — prices, balances, txns, PnL, SQL. [`agents.allium.so`](https://agents.allium.so) · [docs](https://docs.allium.so)
- `dune` — SQL on raw blockchain data — txns, events, stablecoin flows, RWAs, DeFi, NFTs. [`api.dune.com`](https://api.dune.com) · [docs](https://docs.dune.com/api-reference/agents/mpp)
- `codex` — Onchain GraphQL — prices, charts, trades, wallets across 80+ chains. [`graph.codex.io`](https://graph.codex.io) · [docs](https://docs.codex.io)
- `nansen` — Smart-money intelligence, wallet profiling, DEX flows, PnL. [`api.nansen.ai`](https://api.nansen.ai) · [docs](https://docs.nansen.ai)
- `alchemy` — Core RPC + Prices + Portfolio + NFT APIs across 100+ chains. [`mpp.alchemy.com`](https://mpp.alchemy.com) · [docs](https://agents.alchemy.com/s)
- `quicknode` — Core node API across 80+ blockchains / 140+ networks. [`mpp.quicknode.com`](https://mpp.quicknode.com) · [docs](https://quicknode.com/)
- `rpc` — Tempo mainnet / testnet JSON-RPC. [`rpc.mpp.tempo.xyz`](https://rpc.mpp.tempo.xyz) · [docs](https://docs.tempo.xyz)

## Storage / hosting

- `storage` — S3/R2-compatible objects with dynamic per-size pricing. [`storage.mpp.tempo.xyz`](https://storage.mpp.tempo.xyz) · [docs](https://developers.cloudflare.com/r2/)
- `pinata` — Public IPFS pin + fetch via MPP. [`mpp.pinata.cloud`](https://mpp.pinata.cloud) · [docs](https://docs.pinata.cloud/files/mpp/overview)
- `stableupload` — Files + static sites with custom domains (6-month TTL). [`stableupload.dev`](https://stableupload.dev) · [docs](https://stableupload.dev)
- `codestorage` — Paid Git repos — create + get authenticated clone URLs. [`codestorage.mpp.tempo.xyz`](https://codestorage.mpp.tempo.xyz) · [docs](https://code.storage)

## Compute

- `modal` — Serverless GPU compute, sandboxed code execution, ML workloads. [`modal.mpp.tempo.xyz`](https://modal.mpp.tempo.xyz) · [docs](https://modal.com/docs)
- `judge0` — Sandboxed code execution in 60+ languages. [`judge0.mpp.paywithlocus.com`](https://judge0.mpp.paywithlocus.com) · [docs](https://ce.judge0.com)
- `buildwithlocus` — Deploy containers + Postgres + Redis + custom domains via REST. [`mpp.buildwithlocus.com`](https://mpp.buildwithlocus.com) · [docs](https://docs.paywithlocus.com/build)

## Communication / messaging

- `agentmail` — Email inboxes for agents — drafts, threads, webhooks, domains. [`mpp.api.agentmail.to`](https://mpp.api.agentmail.to) · [docs](https://docs.agentmail.to)
- `stableemail` — Pay-per-send email + forwarding inboxes; no API keys. [`stableemail.dev`](https://stableemail.dev) · [docs](https://stableemail.dev)

## Translation / OCR / utilities

- `deepl` — Translation across 30+ languages + DeepL Write rephrasing. [`deepl.mpp.paywithlocus.com`](https://deepl.mpp.paywithlocus.com) · [docs](https://developers.deepl.com)
- `mathpix` — OCR for math, science, documents — LaTeX / MathML / Markdown. [`mathpix.mpp.paywithlocus.com`](https://mathpix.mpp.paywithlocus.com) · [docs](https://docs.mathpix.com)
- `screenshotone` — Capture any URL/HTML/markdown as PNG/JPEG/WebP/PDF. [`screenshotone.mpp.paywithlocus.com`](https://screenshotone.mpp.paywithlocus.com) · [docs](https://screenshotone.com/docs/getting-started/)
- `twocaptcha` — Solve reCAPTCHA, Turnstile, hCaptcha, image captchas. [`twocaptcha.mpp.tempo.xyz`](https://twocaptcha.mpp.tempo.xyz) · [docs](https://2captcha.com)

## Real-world / fun

- `billboard` — Post to @MPPBillboard on X. Starts at $0.01, **doubles each post**. [`billboard.mpp.paywithlocus.com`](https://billboard.mpp.paywithlocus.com) · [docs](https://x.com/MPPBillboard)
- `prospect-butcher` — Order a sandwich for pickup in Brooklyn (first food purchase by an AI agent). [`agents.prospectbutcher.shop`](https://agents.prospectbutcher.shop) · [docs](https://agents.prospectbutcher.shop)
- `doma` — Register a real `.com` / `.xyz` / `.ai` / `.io` / `.net` onchain (~$13+, real money). [`mpp.doma.xyz`](https://mpp.doma.xyz) · [docs](https://docs.doma.xyz)
- `stripe-climate` — Fund permanent carbon removal. [`climate.stripe.dev`](https://climate.stripe.dev) · [docs](https://climate.stripe.dev)
- `papercut` — Roast postcards by your agent (digital or physical) — **physical needs a mailing address**. [`papercut.lol`](https://papercut.lol) · [docs](https://papercut.lol)

## Travel

- `stabletravel` — Flights / hotels / activities / transfers / live tracking (Amadeus + FlightAware). [`stabletravel.dev`](https://stabletravel.dev) · [docs](https://stabletravel.dev)
- `aviationstack` — Real-time + historical flight tracking, airports, airlines, schedules. [`aviationstack.mpp.tempo.xyz`](https://aviationstack.mpp.tempo.xyz) · [docs](https://api.aviationstack.com)
- `flightapi` — Flight prices, tracking, airport schedules — 700+ airlines. [`flightapi.mpp.tempo.xyz`](https://flightapi.mpp.tempo.xyz) · [docs](https://api.flightapi.io)
- `goflightlabs` — Flight tracking, prices, schedules, airline data. [`goflightlabs.mpp.tempo.xyz`](https://goflightlabs.mpp.tempo.xyz) · [docs](https://goflightlabs.com)
- `serpapi` — Google Flights search — prices, schedules, booking options. [`serpapi.mpp.tempo.xyz`](https://serpapi.mpp.tempo.xyz) · [docs](https://serpapi.com)
