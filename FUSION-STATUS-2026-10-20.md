# Synthia / Cynthia fusion source preservation — 2026-10-20

This is a preservation branch. The repository main branch was not modified. No claims are made that these ZIPs form one working Android application.

## Original ZIPs committed byte-for-byte
- `source-archives/FusionEngine.zip`: SHA-256 `32e63f0028ae68ef4bbf1724c49ae27d13709d060e5127b4ca69197c31ff8b77`
- `source-archives/yijing_fusion_output.zip`: SHA-256 `7bda2589e0f7ff76cdd3fbabf729bb3b2a0facedd9fc1b7af73df2541d004553`
- `source-archives/Cynthia_Full_Unified_Progression.zip`: SHA-256 `cf73f31f4df36ab078f409c8b6b1e3244298b606708dd5326373be073d7415d8`

## Source archives not yet pushed
- `CynthiaFusion.zip` (31,791,313 bytes, from user's Drive)
- `GGP_Fused_Brain.zip` (30,353,092 bytes, from user's Drive)
- `Synthia-Generative-Address-Morphology-Integrated-v0.2.1-RUNNABLE-2(1).zip` (user-supplied as a separate source)
Attempts to transfer a large binary through the GitHub connector failed. Do not label the branch a complete migration.

## Synthia integrated v0.2.1 local verification
- `npm run test:all`: 11 root + 29 execution + 6 trainable tests passed.
- `npm --prefix extensions/generative-address-morphology test`: 5/5 passed.
- Integrated server smoke: GET `/api/audit`, `/`, `/app.js` returned 200.
- POST `/api/chat` in Klein and Morph modes returned 200 and different processing paths.
- Communication mode returned 409 intentionally; it belongs to the preserved v14 UI's direct transport.

## Android APK status
No APK has been built. The standalone Synthia v0.2.1 includes Node.js-dependent local server modules (`node:http`, `node:fs`, `node:crypto`), not an Android project. A WebView-only shell would leave Klein/Morph without a local core and is not a valid complete build. Android runtime packaging, local-core wiring, and device smoke tests must succeed before claiming an installable APK.

No existing app architecture was replaced to work around this.
