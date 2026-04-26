# ns-ppc-workshop

Hands-on materials for *Pay-per-Call: When Agents Can Pay* — a workshop at [Network School](https://ns.com), hosted by [@pepyakin](https://x.com/pepyakin).

You walked into a room where every agent was given a small pile of money and told to make something. This repo is the brief.

## Quickstart

1. Pick the 6-character referral code you called out from the slide.
2. Open https://wallet.tempo.xyz/, register a wallet, then **Add Funds** → **Claim referral code** → enter your code → **Claim**.

   > The passkey you save during registration is your way back into the wallet — note where it lands (Keychain, 1Password, browser).

3. Clone this repo and `cd` into it:
   ```
   git clone https://github.com/pepyakin/ns-ppc-workshop.git
   cd ns-ppc-workshop
   ```
4. Open your agent (Claude Code, Cursor, OpenClaw, etc.) in that directory and tell it:

   > Read AGENTS.md and follow it.

That's it — the agent installs the tempo CLI, verifies your balance, and helps you build something.

> **If your agent says balance is 0 and reaches for `tempo wallet fund`** — that's a faucet/bridge, *not* a referral redemption. Go back to step 2 and claim the code in the browser.

## What you need

- **Laptop with an agent set up.** [Claude Code](https://docs.claude.com/en/docs/claude-code/overview) install: `curl -fsSL https://claude.ai/install.sh | bash`, then `claude` in any directory.
- **No laptop?** Pair up. Co-driving is fine. Spectating is fine.

## What to build

Three seed ideas. Pick one or invent your own — anything that strings together a couple of paid services into a small useful (or absurd) result counts.

### A. Country-style weather song

Agent looks up the local forecast, writes country-style lyrics about it, generates the song.

Suggested services: **OpenWeather** for forecast, any LLM (**Anthropic** / **OpenAI** / **Gemini** / **OpenRouter**) for lyrics, **Suno** for the song.

### B. Research pack → Marp deck → here.now

Pick a company or a person. Have your agent compile a 1-pager research pack as a [Marp](https://marp.app) deck and publish it to [here.now](https://here.now). You walk away with a shareable URL.

Suggested services:
- People / company enrichment: **Apollo**, **Hunter**, **Clado** (LinkedIn deep search), **Diffbot KG** (10B+ entities), **StableEnrich**
- Web research: **Exa**, **Tavily**, **Perplexity**, **Firecrawl**, **Brave**, **Parallel**
- Tech-stack profiling: **BuiltWith**
- US public filings: **EDGAR**
- Slide copy: any LLM

### C. Bring your own mashup

A few real services worth poking at:

- **Billboard** — post to @MPPBillboard on X. Price starts at $0.01 and **doubles with every post**. Native pay-per-call anti-spam.
- **Prospect Butcher** — order a real sandwich for pickup in Brooklyn (impractical from here but the API works).
- **Doma** — register a real `.com` / `.xyz` / `.ai` / `.io` / `.net` domain onchain. Heads-up: priced in real dollars, ~$13+ per year.
- **Stripe Climate** — fund permanent carbon removal.

## Service catalog

[`services.md`](./services.md) is a curated subset grouped by category. The full live catalog (91 services) is at https://mpp.dev/services. Anything listed there is fair game — point your agent at the `service_url` and let it figure out the rest.

## Show-and-tell

When we regroup, share what you (or your agent) made. A working demo, a result URL, a transcript, a song file, a postcard — whatever.

## Contact

[@pepyakin](https://x.com/pepyakin) on [Telegram](https://t.me/pepyakin) and [X](https://x.com/pepyakin).

## Further reading

- [mpp.dev](https://mpp.dev) — the MPP service catalog ([direct list](https://mpp.dev/services)).
- [mppscan.com](https://www.mppscan.com/) — MPP ecosystem traction.
- [paymentauth.org](https://paymentauth.org/) — the IETF spec.
- [tempo.xyz](https://tempo.xyz/)
- [Micropayments and Mental Transaction Costs](https://nakamotoinstitute.org/library/micropayments-and-mental-transaction-costs/) — Nick Szabo on why micropayments mostly failed.
