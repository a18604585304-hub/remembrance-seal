# Founding circuit: ALLOW-ONCE Remembrance Gate

**Status:** taped out on X Layer  
**Circuit ID:** `#1`  
**Processor:** `0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239`  
**Tx:** `0xa2999e72f48727f8682d1848f3141aa7f4e69c7aad00c749881f7f0ce3a82f24`  
**Page:** https://tapeout.net/#l2account/xlayer/0x0dba1bcb8abdc1be2a0a2f9d9ddc745f32297239/1

## Intent

A permission that can be sealed into memory:

> Once `intent` and `arm` are both true, the output stays true.

## Pins

| | |
|--|--|
| nIn | 2 (`intent`, `arm`) |
| nOut | 1 (`remembered_allow`) |
| nState | 1 (D-latch) |
| gateCount | 8 (7 NAND + 1 LATCH) |

## Logic

```text
and = AND(intent, arm)           // NAND then NOT
d   = OR(q, and)
q   = LATCH(d)                   // remembrance
out = identity(q)                // official double-NOT output buffer
```

Burned: 7 NAND transistors + 1 LATCH transistor from the Agent wallet.

## Metaphor

- `intent` = the Agent wants to act
- `arm` = the seal press is armed
- latched `1` = the permission has been remembered and cannot be silently forgotten
