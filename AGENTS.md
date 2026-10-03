# Documentation project instructions

- Mintlify site. Pages are MDX; navigation is in `docs.json`.
- Preview with `mint dev` and check links with `mint broken-links`. The Mintlify CLI does not run on Node 25; use `npx -y node@22 $(which mint) broken-links`.
- The current working tree in `../program/programs/gabox/src` and `../program/programs/gabox-hook/src` is the source for rules. Use `../gabox-sdk/src` for client behavior. Both may be ahead of `../program/README.md` and `DEPLOYMENT.md`. The Mega Pack lives on the program's `mega-pack` branch (`../worktrees/program-mega`, with `docs/mega-design.md` and `docs/mega-interfaces.md`) until it merges into `main`.
- `../gabox-app` is the source for what the app shows: pack prices, the create page and the Mega Pack screens.
- `../program/DEPLOYMENT.md` is the source for what was actually deployed. Separate implemented behavior from confirmed deployment.
- Do not copy examples or numbers from older Gabox versions. Verify constants and formulas in source.
- Use short, direct sentences. Explain a technical term on first use. Use `machine`, `pack`, `coin`, `buyer`, `creator`, `holder`, `prize row`, `vault`, and `draw` consistently. Write at CEFR B2 level: one idea per sentence, plain words, active voice.
- Packs have fixed USDC prices ($10, $50, $200, $500, $1,000), and buyers pay in USDC. Inside the program, amounts are in the machine's quote token, which may be USDC, SOL or a registered stock token. Do not promise a cash return.
- Keep each page focused. Use a diagram when it clarifies an order of events or a trust boundary.
- Do not publish internal keys, test wallets, or private RPC endpoints.
