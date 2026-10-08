# Documentation project instructions

- Mintlify site. Pages are MDX; navigation is in `docs.json`.
- Preview with `mint dev` and check links with `mint broken-links`. The Mintlify CLI does not run on Node 25; use `npx -y node@22 $(which mint) broken-links`.
- The current working tree in `../program/programs/gabox/src` and `../program/programs/gabox-hook/src` is the source for rules. Use `../gabox-sdk/src` for client behavior. Both may be ahead of `../program/README.md` and `DEPLOYMENT.md`. The Mega Pack rounds (quote-token rewards) are on the program's `main`. Their plan is `../program/docs/mega-pack-plan.md`; its "Decisions of October 5, 2026" section wins over the body. `docs/mega-design.md` describes the earlier coin-buying Mega Pack and is history only.
- `../gabox-app` is the source for what the app shows: pack prices, the create page and the Mega Pack screens.
- `../program/DEPLOYMENT.md` is the source for what was actually deployed. Separate implemented behavior from confirmed deployment.
- Do not copy examples or numbers from older Gabox versions. Verify constants and formulas in source.
- Use short, direct sentences. Explain a technical term on first use. Use `machine`, `pack`, `coin`, `buyer`, `creator`, `holder`, `prize row`, `vault`, and `draw` consistently. Write at CEFR B2 level: one idea per sentence, plain words, active voice.
- Packs have fixed USDC prices from a fixed range, and buyers pay in USDC. Do not list the exact pack prices: they may change. Say "a fixed range of pack prices" and "the largest pack". Escape a dollar sign before a digit as `\$` (an unescaped pair renders as LaTeX math). Inside the program, amounts are in the machine's quote token, which may be USDC, SOL, a registered stock token or another registered Solana token. Do not promise a cash return.
- `brand-kit.mdx` and the files in `brand/` come from `../gabox-app`: `public/` for the logos and icons, `app/globals.css` and `docs/DESIGN.md` for colors and type. Keep the hex values in step with the app's OKLCH tokens.
- Keep each page focused. Use a diagram when it clarifies an order of events or a trust boundary.
- Do not publish internal keys, test wallets, or private RPC endpoints.
- Do not describe security weak points or how to get around a guard: no upgrade-key setup, no checks the program leaves to off-chain services, no operator or snapshot timing, no exploit-style examples. Say what the program enforces and how users can verify it.
