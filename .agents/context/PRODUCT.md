# Gabox docs

## Register

product

## What this is

The documentation site for Gabox, an onchain gacha protocol on Solana. A **machine** is a gacha
pool bound to one brand-new coin. Buyers open **packs** of that coin and win a prize from an
immutable prize table. Randomness comes from MagicBlock VRF. The site is built on Mintlify and
lives at the same brand as the app (gabox.fun).

## Who reads it

1. **Buyers**: people who open packs. They want to know what a pack costs, what it can win, how
   likely each prize is, and what happens if something goes wrong. Many are not native English
   readers. Write at CEFR B2.
2. **Creators**: people who launch a coin and its machine. They want to know what they choose,
   what they pay for the seed, what they earn, and what they can never change.
3. **Developers and reviewers**: people who read the program or build on the SDK. They want exact
   constants, account layouts, invariants, and the math.

## Purpose

Make the mechanism understandable and checkable. Every claim about odds, fees, or safety must
point at a constant, a formula, or an instruction in the program. No marketing claims about
returns. No US dollar amounts. Amounts are tokens or SOL.

## Brand personality

Calm, exact, confident. The app's line is "the lights-down drop": a near-black room with one
electric lime signal. The docs carry the same room and the same signal, but the signal is used
for structure (links, active nav, one accent in a diagram), never for decoration.

## Anti-references

- Casino copy: "win big", "jackpot mania", exclamation marks, countdown urgency.
- Crypto-generic docs: gradient text, glass cards, numbered eyebrows on every section.
- Dense terminal aesthetics: monospace everything, walls of hex.
- Any mention of the market vendor by name. The docs say "the coin's own market".

## Strategic design principles

1. **One term per concept.** The Terminology table in `AGENTS.md` is the contract.
2. **Numbers before adjectives.** Show the table, then explain it.
3. **Every page answers one question**, named in its description. If a page needs two, split it.
4. **Diagrams show the real mechanism.** No decorative art. Every node names a real actor or
   account.
5. **Disclose the downside on the same page as the upside.** Expected return, timeouts, and price
   risk sit next to the prize table, not in a legal appendix.
