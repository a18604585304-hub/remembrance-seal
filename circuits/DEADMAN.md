# Circuit #2: DEADMAN heartbeat gate

**Status:** taped out on X Layer  
**Circuit ID:** `#2`  
**Processor:** `0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239`  
**Tx:** `0xd4fd8467445d3a046fef190eff3851c52e6cb324dee1b094f13b9a701948e146`  
**Page:** https://tapeout.net/#l2account/xlayer/0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239/2

## Intent

Keep the seal unlocked only while a heartbeat keeps arriving.

> Arm once, then keep beating. Miss a beat → latched dead until re-armed.

## Pins

| | |
|--|--|
| nIn | 2 (`arm`, `beat`) |
| nOut | 1 (`alive`) |
| nState | 1 (D-latch) |
| gateCount | 8 (7 NAND + 1 LATCH) |

## Logic

```text
d   = OR(arm, AND(q, beat))
q   = LATCH(d)
out = identity(q)
```

- `arm=1` → force alive
- `alive` and `beat=1` → stay alive
- `alive` and `beat=0` → die on the next step
- dead stays dead until `arm` again

## Metaphor

Insurance imprint on the same seal press as ALLOW-ONCE.  
Missed heartbeat can later key vault lock / burn / routing — this circuit is the on-chain flip, not the vault itself.
