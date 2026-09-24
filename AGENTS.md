# Documentation project instructions

- Mintlify site. Pages are MDX; navigation is in `docs.json`.
- Preview with `mint dev` and check links with `mint broken-links`.
- The current working tree in `../program/programs/gabox/src` and `../program/programs/gabox-hook/src` is the source for rules. Use `../gabox-sdk/src` for client behavior. Both may be ahead of `../program/README.md` and `DEPLOYMENT.md`.
- `../program/DEPLOYMENT.md` is the source for what was actually deployed. Separate implemented behavior from confirmed deployment.
- Do not copy examples or numbers from older Gabox versions. Verify constants and formulas in source.
- Use short, direct sentences. Explain a technical term on first use. Use `machine`, `pack`, `buyer`, `creator`, `prize row`, `vault`, and `draw` consistently.
- Describe costs in the machine's quote asset, which may be SOL or another registered token. Do not promise a cash return.
- Keep each page focused. Use a diagram when it clarifies an order of events or a trust boundary.
- Do not publish internal keys, test wallets, or private RPC endpoints.
