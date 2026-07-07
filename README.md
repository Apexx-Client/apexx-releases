# apexx-releases

Encrypted Apexx client payloads for gated delivery.

Each `apexx-client-<version>.enc` is the client jar encrypted with AES-256-GCM
(layout: `nonce(12) || ciphertext || tag(16)`), produced by the website's
`scripts/encrypt-payload.mjs`. The blob is opaque without the key: the website's
`/api/download` (and the loader's `/api/client`) hand the decryption key ONLY to
authenticated paid users, who decrypt it client-side.

Do not commit plaintext jars here.

| Version | File | Plaintext SHA-256 |
|---|---|---|
| 4.3.5 | `apexx-client-4.3.5.enc` | `c46090868ad35914aacda5cceedb2d1febecb80c90810b46765dedfb39e17ba1` |
