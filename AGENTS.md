# Agent guide — Network School Pay-per-Call workshop

You're in a workshop participant's cloned workspace. Your job: install the tempo wallet, confirm the user has funds, then help them build a small mashup using paid services.

## 0. Setup (do this first)

1. Read https://tempo.xyz/SKILL.md and follow it. Specifically:
   - Install with `curl -fsSL https://tempo.xyz/install | bash` (places the CLI at `$HOME/.tempo/bin/tempo`).
   - Run `tempo wallet login` — this opens a browser; the user authenticates with the same passkey they registered at https://wallet.tempo.xyz/.
   - Verify with `tempo wallet -t whoami`.
2. Inspect the `whoami` balance.
   - The workshop master seeds each participant with $1 via a referral code.
   - If it's positive → continue to step 1.
   - If it's 0 → tell the user to go to https://wallet.tempo.xyz/ → **Add Funds** → **Claim referral code** → enter the 6-char code from the slide.
   - If the user runs out of funds or needs more mid-session, it's on the table to ask the workshop master for an additional referral code.
   - **Do NOT run `tempo wallet fund`.** That's a testnet faucet / mainnet bridge — not a referral redemption path. Running it will not redeem a referral code.

## 1. Pick something to build

Ask the user which seed idea they want, or what they'd rather do. The full descriptions are 
to be found in the README.md. 

Whatever they pick, scope it small. A single 30-minute session is the budget.

## 2. Discover services

`services.md` has a curated catalog grouped by category. The full live catalog can 
be listed via `tempo wallet -t services --search <query>`.

To inspect a specific service: `tempo wallet -t services <SERVICE_ID>`.

## 3. Make paid requests

Use `tempo request` (per `SKILL.md`):

```
tempo request -t -X POST --json '{"input":"..."}' <SERVICE_URL>/<ENDPOINT_PATH>
```

Always run with `--dry-run` first when:
- the request might be expensive,
- the price is dynamic (e.g., domain registration),
- you're not sure the endpoint will succeed.

`--dry-run` shows the price without actually charging.

## 4. Save artifacts to `./out/`

`out/` is gitignored. Put everything you generate there: rendered HTML, decks, songs, images, output URLs, transcripts. The user shows what's in `out/` during show-and-tell.

For mashup B specifically, the publishing flow is:

1. Write the deck as Marp markdown (e.g., `out/deck.md`).
2. Render: `npx --yes @marp-team/marp-cli@latest out/deck.md --html -o out/deck.html`.
3. Publish to here.now (docs at https://here.now/docs). The 3-step API:
   - `POST https://here.now/api/v1/publish` with a file manifest → returns presigned upload URLs, a finalize URL, and a `siteUrl`. **Save the `claimToken` immediately — it's only returned once.**
   - `PUT` the file body to the presigned URL.
   - `POST` to the returned finalize URL with `{"versionId":"..."}`.

   Alternatively, just tell here.now's hosting layer "publish this to www.here.now" and it can take it from there.

## Conventions

- Re-check `tempo wallet -t whoami` before and after large payments so the user can see what was spent.
- If a service looks US-gated (KYC, domestic phone numbers, US addresses), warn the user before trying. Known geo-locked services: `stablephone`, `postalform`, `martin-estate`. `papercut` requires an address and is awkward for live demos.
- Don't run anything destructive without asking.
- When you finish, surface the artifact (URL, file path) clearly so the user can demo it.
