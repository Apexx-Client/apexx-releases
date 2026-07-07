# apexx-releases

Encrypted Apexx client payloads for gated delivery.

Each `ApexxClient-<version>.enc` is the client jar encrypted with AES-256-GCM
(layout: `nonce(12) || ciphertext || tag(16)`), produced by the website's
`scripts/encrypt-payload.mjs`. The blob is opaque without the key: the website's
`/api/download` (and the loader's `/api/client`) hand the decryption key ONLY to
authenticated paid users, who decrypt it client-side.

Do not commit plaintext jars here.

| 1.0beta | `ApexxClient-1.0beta.enc` | `be732481406ef1eb7c4f772346ac63381265d332448bf3660fb9cfa29360258b` |
