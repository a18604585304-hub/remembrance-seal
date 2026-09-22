# Remembrance Seal

> An OKX.AI Agent's on-chain corporate seal.  
> Transistors are blank seals. Taped-out circuits are irreversible permission memories.

**Hackathon:** TapeOut Genesis Transistor Hackathon (Ignix × TapeOut × X Layer)  
**Chain:** X Layer  
**Brand:** Remembrance Seal  
**Stack:** Agent Seal × Remembrance Gate × Mood ASIC × Dead Man Switch

---

## One-line pitch

Most processors mint transistors to speculate.  
**Remembrance Seal** mints transistors to *authorize*.

It is a **seal factory** for one-person companies on OKX.AI:
- **Processor** = the company's seal press
- **Transistor** = a blank seal unit (authority inventory)
- **Circuit (tape-out)** = a sealed imprint that cannot be rewritten

---

## Seal Stack (four capabilities, one product)

Do not read this as four unrelated memes. It is one permission OS:

```text
L4  Agent Seal          who uses the press     OKX.AI one-person company
L1  Remembrance Gate    what a seal means      irreversible ALLOW / DENY
L2  Mood ASIC           a specialized imprint  FOMO / FEAR / HOLD / EXIT
L3  Dead Man Switch     a specialized imprint  heartbeat timeout → lock / burn / vault
     TapeOut Processor  the factory on X Layer
```

| Layer | Original idea | Role in the product | Hackathon delivery |
|-------|---------------|---------------------|--------------------|
| **L4** | Agent Seal | Who the factory belongs to | Bind existing OKX.AI ASP Agents |
| **L1** | Remembrance Gate | Nature of every imprint | **Must tape `ALLOW-ONCE`** |
| **L2** | Mood ASIC | Strategy imprint | Spec + optional later circuit |
| **L3** | Dead Man Switch | Insurance imprint | Spec + optional later circuit |

Ignix Genesis angle: if this transistor becomes Genesis-adjacent, vault release / buyback / dividend routing can key off **sealed circuit outputs**, not admin keys.

---

## 30-second intro

Most TapeOut projects manufacture speculative transistors.  
We manufacture **Agent permission infrastructure**.

Remembrance Seal deploys a seal processor on X Layer:
- mint transistors = expand seal quota
- tape out a circuit = press an irreversible permission memory

It serves OKX.AI Agents already operated as one-person companies.  
The same seal can later carry two specialized imprints:
- **Mood** — encode FOMO/FEAR as callable policy states for Ignix vaults
- **Dead Man** — if heartbeat stops, output flips and funds lock / burn / enter vault

Hackathon window: a live factory + founding Remembrance Gate.  
Mood and Dead Man are protocol extensions, not a second project.

---

## Architecture

```text
OKX.AI Agent (one-person company)
        │
        ▼
Remembrance Seal Processor  (TapeOut · X Layer)
        │
        ├── mint transistors  →  authority inventory
        │
        └── tape out circuit  →  Seal Imprint (Circuit NFT)
                │
                ├── ALLOW-ONCE   (founding Remembrance Gate)
                ├── MOOD-*       (optional strategy imprint)
                └── DEADMAN-*    (optional insurance imprint)
                        │
                        └── Future: Ignix vault release condition
```

### Founding circuit (MVP)

**Name:** `ALLOW-ONCE`

Minimal canvas version:
1. Two inputs: `intent`, `arm`
2. NAND (or equivalent) + optional LATCH for memory
3. One output: `remembered_allow`
4. Tape out on this processor so the Circuit NFT lives under Remembrance Seal

Judging FAQ: circuits can be taped by anyone on the processor. We tape the founding seal ourselves.

---

## Transistor economics

| Parameter | Value | Why |
|-----------|-------|-----|
| Chain | X Layer | Hackathon requirement |
| Total transistors | **88,888** | Seal-number; scarce enough to feel intentional |
| Mint price | **0.000066 OKB** | Low participation; self-mint for demo stays cheap |
| Cap / price | Immutable after create | TapeOut factory rule |
| Creator revenue | Mint proceeds to deployer | Standard factory behavior |

Self-demo cost (order of magnitude):
- Create processor ≈ `0.0066 OKB`
- Mint enough transistors for 1 small circuit + buffer = low OKB
- X Layer gas ≈ negligible

---

## Bound Agents (operator already has the identity layer)

Same operator wallet: `0xa66f492f6f4a5a2b028f18355b63ce240940e0e5`

| Agent | ID | Role in the story |
|-------|----|-------------------|
| Market Signal Desk | `#4515` | Actions that should require a seal before auto-copy / size-up |
| Codex Evidence Lab | `#3359` | Research/risk actions that should require a sealed ALLOW |

Remembrance Seal is the missing manufacturing / governance layer for those Agents.

---

## Use cases

1. **Agent permission seal** — before withdraw / publish / spend escrow, require a taped gate for that action class.
2. **Ignix vault condition** — vault policy keys off sealed circuit output.
3. **Mood policy** — FEAR raises buyback; FOMO tightens emission (extension).
4. **Dead-man insurance** — missed heartbeat flips output (extension).
5. **Community remembrance** — members mint blanks and tape covenants as Circuit NFTs.

---

## Hackathon checklist

- [x] Processor deployed on X Layer via TapeOut factory
- [x] Supply + unit price disclosed at deployment
- [x] ≥1 circuit taped out (`ALLOW-ONCE`, circuit #1)
- [x] Clear use case (Seal Stack)
- [ ] Public GitHub + demo + X announcement
- [x] Google Form submitted (Telegram @blmario; X post link can be added later)

### Addresses

| Field | Value |
|-------|-------|
| Project Name | Remembrance Seal |
| Symbol | SEAL |
| Processor (circuits) | `0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239` |
| Transistors | `0x786759759B9483F54D903A0c95901fef5b89CD49` |
| Deployer / Agent wallet | `0xa66f492F6f4A5a2B028F18355B63ce240940E0E5` |
| Create tx | `0x7dac2ac458781780d1786811486a425f36aaa76a97d21417696fba285f47659c` |
| TapeOut page | https://tapeout.net/#l2/xlayer/0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239 |
| Explorer | https://www.oklink.com/xlayer/tx/0x7dac2ac458781780d1786811486a425f36aaa76a97d21417696fba285f47659c |
| Circuit | `#1 ALLOW-ONCE` — TapeID **1.2.183** (2-in / 1-out / 1 latch, 8 gates) |
| Circuit page | https://tapeout.net/#l2account/xlayer/0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239/1 |
| Tapeout tx | `0xa2999e72f48727f8682d1848f3141aa7f4e69c7aad00c749881f7f0ce3a82f24` |
| GitHub | https://github.com/a18604585304-hub/remembrance-seal |
| X | @blmario669 |

---

## Repo map

- `README.md` — vision, stack, economics
- `demo.md` — 3-minute judge script
- `SUBMISSION.md` — Google Form copy
- `X-POST.md` — announcement draft
- `circuits/` — founding gate notes

---

## Disclaimer

Official UI marks X Layer TapeOut as testing stage. Contracts may be unsealed / unaudited. Prototype only. Use funds you can afford to lose.
