# Maintainer notes — Valreb001

## Issue #749 — `parseIntent` accepting a negative/fractional `sourceChainId`

Already fixed on `main`. `sdk/src/validate.ts`'s `parseIntent` validates
`sourceChainId` with `asPositiveInteger(v.sourceChainId, "intent.sourceChainId")`,
the same constraint `validateIntent` in `sdk/src/intent.ts` applies
(`Number.isInteger(...) && > 0`). A negative, zero, or fractional
`sourceChainId` from the mempool is now rejected with a `MempoolResponseError`
naming the field, matching the outbound rule. No change needed.
