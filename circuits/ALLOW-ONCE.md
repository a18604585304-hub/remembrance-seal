# Founding circuit: ALLOW-ONCE Remembrance Gate

## Intent
Smallest circuit that still expresses the product metaphor:
> A permission that can be sealed into memory.

## Canvas build (MVP)

1. Place **2 Inputs**: `intent`, `arm`
2. Place **1 NAND** (or equivalent composite) combining them
3. Optional: place **1 LATCH** to express remembered state
4. Place **1 Output**: `remembered_allow`
5. Wire:
   - `intent` + `arm` → logic → (`LATCH`) → `remembered_allow`
6. Simulate off-chain until output behaves as expected
7. Select processor **Remembrance Seal** on **X Layer**
8. Tape Out (burns transistors; mints Circuit NFT)

## Naming on-chain / in UI
- Circuit title: `ALLOW-ONCE`
- Story tag: `founding remembrance gate for Agent seal`

## Success criteria
- Circuit appears under Remembrance Seal processor
- Explorer / TapeOut page shows ≥1 circuit
- Demo script can point at it in <60 seconds
