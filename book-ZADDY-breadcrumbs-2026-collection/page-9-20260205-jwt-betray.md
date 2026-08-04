## record: 2026-02-05 · jwt-betray
**title:** JWT Trust Betrayed

tags: `#jwt-security` `#cve-2018-0114` `#jwk-injection` `#node-jose` `#authentication-bypass` `#pentesterlab`
vibe: trust betrayed

- **observed:** Node-jose JWT verification library (<0.11) implicitly trusted client-supplied `jwk` public keys embedded directly within the JWT header.
- **applied:** generated an attacker RSA keypair, injected public parameters (`n`, `e`) into the token header's `jwk` parameter, and signed payload `"admin"` with the attacker private key.
- **concluded:** server validated token signature using embedded attacker key, enabling full administrative authentication bypass without needing server private keys.

refs: [medium](https://dr-kb.medium.com/jwt-trust-betrayed-f91d6715b23c) · [github](https://github.com/bkornpob/pentesterlab/blob/main/cve-2018-0114/formal-writeup.md)

<button class="play-btn" onclick="playStory('../audios/page-9-jwt-trust-betrayed-edgetts-Luke.mp3')">▶ play</button>
