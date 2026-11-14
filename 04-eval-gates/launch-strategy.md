# Module 4 · Launch Strategy · Ascend IQ Copilot

## 4.0 Release Criteria

| Gate | Failure | Metric | Threshold | Dataset | Method | Runs at |
|---|---|---|---|---|---|---|
| Hard | wrong pricing (#HALLUCINATION) | Match correct price with source reliability | 100 | Ascend IQ golden set | Human review | Staging |
| Soft | Row 3 · Latency: exceeded the maximum response time | Wrong prices responses  Performance | 95 | Ascend IQ golden set | Code-based check | Staging |
| Advisory | Row 5 · Hallucination: lists an unconfirmed speaker as confirmed | Incorrect data response | 100 | Ascend IQ golden set | Human review | Pull Request |

## CI Gate Request for Engineering

- **Hard gate · wrong pricing (#HALLUCINATION).** Check: the human review, run on the Ascend IQ golden set at Staging. Measures: Match correct price with source reliability. Passes when: 100. On a fail: block the merge.
- **Soft gate · Row 3 · Latency: exceeded the maximum response time.** Check: the code-based check, run on the Ascend IQ golden set at Staging. Measures: Wrong prices responses  Performance. Passes when: 95. On a fail: pause the release until the PM signs off on an override.
- **Advisory gate · Row 5 · Hallucination: lists an unconfirmed speaker as confirmed.** Check: the human review, run on the Ascend IQ golden set at Pull Request. Measures: Incorrect data response. Passes when: 100. On a fail: post a warning, and don't block.

## Mitigation Plan · Soft Gate

If our Soft gate fails (latency is 4.5 seconds), I recommend a staged rollout because it will allow us to limit the slow answers to our internal team while we collect more data.
