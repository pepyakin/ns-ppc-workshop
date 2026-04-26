# ns-ppc-workshop

Hands-on materials for *Pay-per-Call: When Agents Can Pay* — a workshop at [Network School](https://ns.com), hosted by [@pepyakin](https://x.com/pepyakin).

You walked into a room where every agent was given a small pile of money and told to make something. This repo is the brief.

## Quickstart

1. Pick the 6-character referral code you called out from the slide.
2. Open https://wallet.tempo.xyz/, register a wallet, then **Add Funds** → **Claim referral code** → enter your code → **Claim**.
3. Clone this repo and `cd` into it:
   ```
   git clone https://github.com/pepyakin/ns-ppc-workshop.git
   cd ns-ppc-workshop
   ```
4. Open your agent (Claude Code, Cursor, OpenClaw, etc.) in that directory and tell it:

   > Read AGENTS.md and follow it.

That's it — the agent installs the tempo CLI, verifies your balance, and helps you build something.

> [!IMPORTANT]
> The passkey you save during wallet registration is your way back in — note where it lands (Keychain, 1Password, browser).

## What you need

- **Laptop with an agent set up.** [Claude Code](https://docs.claude.com/en/docs/claude-code/overview) install: `curl -fsSL https://claude.ai/install.sh | bash`, then `claude` in any directory.
- **No laptop?** Pair up. Co-driving is fine. Spectating is fine.

## What to build

Below are three prompts you can copy-paste. But the real fun is writing your own — chain a couple of paid services into something useful, useless, or absurd. All three count.

<details>

<summary><b>Sing today's forecast</b></summary>

> Use ifconfig.me to lookup my ip. Using an mpp service lookup its geo location. After you obtain it get me the forecast for this week. Then create a song in a country style using Suno, let suno generate the lyrics. Then generate an appropriate cover image for this single.

</details>

<details>

<summary><b>Deck a real person</b></summary>

> Create a slide deck about Patrick Collison and his Stripe. Do a proper due dillegence. Find pictures of him and of this company and put them into the slides. When you finish host it annonymously on here.now. For slides use MARP.

</details>

<details>

<summary><b>Land a fake product</b></summary>

> Come up with a landing page for a fake product: tape for mouth for losing weight. The landing page must be well designed. Colorful. Generate people happily using the product. Iterate on the images. Deploy to here.now and double-check the result.

</details>

### Some other one offs:

- **Billboard** — post to @MPPBillboard on X. Price starts at $0.01 and **doubles with every post**. Native pay-per-call anti-spam.
- **Doma** — register a real `.com` / `.xyz` / `.ai` / `.io` / `.net` domain onchain. Heads-up: priced in real dollars, ~$13+ per year.
- **Stripe Climate** — fund permanent carbon removal.

## Service catalog

[`services.md`](./services.md) is a curated subset grouped by category. Anything listed there is fair game — point your agent at the `service_url` and let it figure out the rest.

## Show-and-tell

When we regroup, share what you (or your agent) made. A working demo, a result URL, a transcript, a song file, a postcard — whatever.

## Contact

[@pepyakin](https://x.com/pepyakin) on [Telegram](https://t.me/pepyakin) and [X](https://x.com/pepyakin).

## Further reading

- [mpp.dev](https://mpp.dev) — the MPP service catalog ([direct list](https://mpp.dev/services)).
- [awesome-mpp](https://github.com/mbeato/awesome-mpp) — community-maintained list of MPP services and demos.
- [mppscan.com](https://www.mppscan.com/) — MPP ecosystem traction.
- [paymentauth.org](https://paymentauth.org/) — the IETF spec.
- [tempo.xyz](https://tempo.xyz/)
- [Micropayments and Mental Transaction Costs](https://nakamotoinstitute.org/library/micropayments-and-mental-transaction-costs/) — Nick Szabo on why micropayments mostly failed.
