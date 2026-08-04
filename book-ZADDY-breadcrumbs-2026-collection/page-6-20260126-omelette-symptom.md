## record: 2026-01-26 · omelette-symptom
**title:** When Your AI Guard Can't Tell an Omelette from a Drug

tags: `#ai-security` `#jailbreak` `#rlhf` `#template-guard` `#red-team` `#blue-team` `#service-security-tradeoffs`
vibe: template-guard and rlhf-class vulnerability

- **observed:** RLHF guardrails overfit to syntactic jailbreak templates, causing false positives that block benign requests (e.g., cooking an omelette) when framed in flagged structures.
- **applied:** formalized the `#TEMPLATE-GUARD` vulnerability class, demonstrating how semantic intent (cooking) is ignored while syntactic form triggers hard rejections.
- **concluded:** threshold-based template matching filters are inherently evadable via semantic-preserving perturbations (character/word disguises and structural shuffles).

refs: [medium](https://dr-kb.medium.com/when-your-ai-guard-cant-tell-an-omelette-from-a-drug-a-case-study-for-rlhf-vulnerability-class-a931d9dd5152) · [github](https://github.com/bkornpob/GUARD_TYPE/blob/main/GUARD-1-template-guard.md)

<button class="play-btn" onclick="playStory('../audios/page-6-omelette-symptom-edgetts-Luke.mp3')">▶ play</button>
