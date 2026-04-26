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

### Cap session deposits with `--max-spend`

Some services (LLMs like `gemini`, `openai`, `openrouter`, `anthropic`, etc. — anything with `intent: session` in `tempo wallet -t services <id>`) auto-open a payment channel on first use. The CLI default deposits **$1.00** per channel, which gets locked until the session is closed. With only $1 of workshop budget, a single default-deposit channel eats the whole bag.

Pass `--max-spend` on session-priced calls to cap the deposit (the flag sets the deposit 1:1, not just a per-call ceiling):

```
tempo request -t --max-spend 0.20 -X POST --json '{...}' <SERVICE_URL>/<ENDPOINT_PATH>
```

`$0.20` is a sensible default for workshop calls. Use a smaller value (e.g. `0.05`) for one-off cheap calls, larger if you know you'll make many calls to the same origin.

When you're done with a session-priced service — or at the end of the workshop — run `tempo wallet sessions close --all` to recover any unused deposit back to the wallet's available balance.

## 4. Save artifacts to `./out/<codename>/`

`out/` is gitignored. **Before writing the first artifact, pick a short kebab-case codename for the build and `mkdir -p out/<codename>/`.** Everything you generate — rendered HTML, decks, songs, images, output URLs, transcripts, intermediate JSON — goes under that folder, never directly into `out/`. Workshop participants run multiple builds across sessions, and a flat `out/` quickly becomes an unreadable junk drawer of mixed projects.

Pick the codename from the build itself (e.g. `porch-in-petaling` for a song about that, `brothers-deck` for a slide deck about brothers). If `out/` already has subfolders, glance at them first to avoid name collisions and to orient yourself on prior work.

The user shows what's in `out/<codename>/` during show-and-tell.

For mashup B specifically, the publishing flow is:

1. Write the deck as Marp markdown (e.g., `out/<codename>/deck.md`).
2. Render: `npx --yes @marp-team/marp-cli@latest out/<codename>/deck.md --html -o out/<codename>/deck.html`.
3. Publish to here.now (docs at https://here.now/docs). The 3-step API:
   - `POST https://here.now/api/v1/publish` with a file manifest → returns presigned upload URLs, a finalize URL, and a `siteUrl`. **Save the `claimToken` immediately — it's only returned once.**
   - `PUT` the file body to the presigned URL.
   - `POST` to the returned finalize URL with `{"versionId":"..."}`.

   Alternatively, just tell here.now's hosting layer "publish this to www.here.now" and it can take it from there.

## Conventions

- Re-check `tempo wallet -t whoami` before and after large payments so the user can see what was spent. Note that `locked` funds (sitting in open session channels) are not part of `available` — if `available` looks low, check `tempo wallet -t sessions list` for what's tied up where.
- Run `tempo wallet -t sessions list` after the first call to a session-priced service to confirm the deposit is what you expected (e.g. `0.20`, not the default `1.00`). If a default-deposit channel slipped through, close it with `tempo wallet sessions close <origin-or-channel-id>` and re-call with `--max-spend`.
- At the end of the workshop (or whenever the user runs out of budget), run `tempo wallet sessions close --all` to return locked deposits to the available balance.
- Don't run anything destructive without asking.
- When you finish, surface the artifact (URL, file path) clearly so the user can demo it.
