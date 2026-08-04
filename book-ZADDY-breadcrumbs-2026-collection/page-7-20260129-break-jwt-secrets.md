## record: 2026-01-29 · break-jwt-secrets
**title:** Breaking JWT Secrets

tags: `#jwt-security` `#secret-brute-force` `#authentication-bypass` `#pentesterlab` `#web-security`
vibe: offline secret brute force

- **observed:** web application used weak, guessable secret keys to sign JSON Web Tokens (`auth` cookie).
- **applied:** performed offline dictionary brute-force attack against token signature to recover secret (`pentesterlab`), then forged new payload `{ "user": "admin" }`.
- **concluded:** recovered secret key allowed full administrative authentication bypass and privilege escalation without backend access.

refs: [medium](https://dr-kb.medium.com/breaking-jwt-secrets-35d78ee2fb4b) · [github](https://github.com/bkornpob/pentesterlab/blob/main/jwt-v/formal-writeup.md)

<button class="play-btn" onclick="playStory('../audios/page-7-break-jwt-secrets-edgetts-Luke.mp3')">▶ play</button>
