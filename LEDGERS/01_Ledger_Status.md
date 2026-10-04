# Ledger Status

**Project:** `L_WORLDSIM`  
**Tier:** TIER_5_WORLD_NEURO_EMBODIED  
**Identity:** Upstream `4thfever/cultivation-world-simulator` @ `471fe745e7c3` (CC-BY-NC-SA-4.0)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `4thfever/cultivation-world-simulator` |
| Commit | `471fe745e7c3d582048d647257c74ae566cd235f` |
| Upstream licence | CC-BY-NC-SA-4.0 |
| Licence class | restricted |
| Clone size | 367.36 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 0 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
