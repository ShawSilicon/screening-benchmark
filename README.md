# Chip design screening: methodology and first results

**ShawSilicon. Data cut 2 August 2026. Report version 0.1.**

Nobody publishes pass and fail rates for semiconductor technical screening. Recruiters do not measure it, employers do not release it, and assessment vendors have no reason to tell you how many people fail. So there is no public baseline for what a real chip design screen filters out.

This report is the beginning of one. It is deliberately small and deliberately honest about what it cannot yet say.

---

## What this report is, and is not

**It is** an outcome-level result at n = 30, a session funnel at n = 22, and a full description of the instrument that produced them.

**It is not** a benchmark. A benchmark needs enough observations to be stable, and this does not have them yet. Everything below carries its n. Nothing is extrapolated, and no percentage appears without the count behind it.

**It does not report per-round failure rates.** We can measure them and we intend to publish them, but the sample is currently one to nine observations per round depending on the round, which is not enough to report. Section 5 states exactly how thin, because a report that hides its own gaps is the thing this company exists to argue against.

---

## 1. The instrument

Engineers complete three rounds in their own specialization.

| Round | What it tests | Scored dimensions |
|---|---|---|
| 1 | Conceptual depth in the specialization | `conceptual_depth` |
| 2 | Applied work sample, code, written reasoning and the design the candidate draws | `design`, `debugging`, `diagrams` |
| 3 | Recorded defence of that design under questioning | `adversarial_debug` |

Five scored dimensions in total. Rounds 1 and 2 combine deterministic checks with model-assisted scoring. Round 3 is reviewed by a practising FPGA engineer.

Question bank: **300 items across the 9 specializations engineers can select** (FPGA design, ASIC design, verification and UVM, formal verification, physical design, analog and mixed-signal, embedded hardware, AI chip architecture, DFT). A further 80 items exist for four specializations not yet exposed in the product and are excluded from that count.

**Pass floor: 51 of 100.**

The rubric weights and the question bank are not published. The round structure, the dimensions and the floor are.

---

## 2. Outcome results, n = 30

Thirty engineers external to the company have a scored result on record.

| | Count |
|---|---|
| Scored | **30** |
| Cleared the 51 floor | **17** |
| Did not clear | **13** |
| **Non-pass rate** | **43.3%** |

### Score distribution, all 30

```
79 78 77 76 75 71 66 66 62 60 60 59 57 55 54 53 51    <- cleared (17)
49 45 45 44 42 42 41 31 27 26 25 22  3                <- did not clear (13)
```

| Band | Count |
|---|---|
| 80 and above | 0 |
| 70 to 79 | 6 |
| 60 to 69 | 5 |
| 51 to 59 | 6 |
| 40 to 50 | 7 |
| 25 to 39 | 4 |
| 24 and below | 2 |

Two observations worth stating plainly. **Nobody has scored 80 or above.** And the distribution below the floor is not clustered just underneath it: seven of the thirteen who did not clear scored below 40, which is a different failure from a near miss.

---

## 3. Session funnel, n = 22

Twenty-two sessions have been started on the three-round flow.

| | Count |
|---|---|
| Sessions started | **22** |
| Submitted both round 1 and round 2 | **9** |
| Abandoned before submitting anything | **13** |
| Graded through all three rounds | **1** |

**Thirteen of twenty-two starts produce no submission at all.** Those candidates opened the screen and left without answering. This is not a pass or fail result, and it is not counted as either, but it is the largest single number in the funnel and we would rather publish it than quietly drop it.

---

## 4. Round 1 results, n = 8

The only round with enough observations to show anything.

`conceptual_depth`, eight scored submissions: **63, 67, 77, 80, 80, 82, 83, 86**

Median 80. Range 63 to 86. This says the population reaching round 1 submission is reasonably strong on fundamentals, which is expected: the drop-off in section 3 happens earlier.

Eight observations. Do not build anything on this.

---

## 5. What we cannot report yet, and how thin it is

| Round | Dimension | Observations |
|---|---|---|
| 1 | `conceptual_depth` | 8 |
| 2 | `design` | 9 |
| 2 | `debugging` | 9 |
| 2 | `diagrams` | **1** |
| 3 | `adversarial_debug` | **1** |

Round 3, and the diagrams dimension, have a single observation each. There is no per-round failure rate to report and there will not be one until the sample supports it.

**One further disclosure.** In the round 2 data, seven of nine `design` scores and seven of nine `debugging` scores are identical values. That pattern is more consistent with a scorer returning a default than with a scorer discriminating between candidates. Until that is investigated and resolved, **no round 2 result should be treated as a measurement**, and none is reported above beyond the raw count. We are stating this rather than publishing a mean that looks meaningful and is not.

---

## 6. Method notes and limitations

- **Selection.** Candidates self-select by registering. This is not a random sample of chip engineers and should not be read as one.
- **Internal accounts excluded.** Company-domain and test accounts are removed from every figure above. Thirty-three scored records exist in total; three are internal and are excluded, leaving 30.
- **Two scoring generations.** The 30 outcome results span an earlier scoring flow and the current three-round flow. The 51 floor applies to both. Per-round data exists only for the current flow, which is why sections 2 and 4 have different n.
- **Scope.** This report covers screening outcomes only. Downstream performance data is out of scope for v0.1.

---

## 7. Why publish this at all

Because the argument ShawSilicon makes rests on a specific claim: that a screen most people pass is not a filter. That claim is worth nothing unless the failure rate is public and checkable.

**43.3% of thirty engineers who completed a scored screen did not clear the bar.** That is the number. It is small, it is early, and it is real.

We will republish as n grows, including when it moves against us.

---

## Corrections and contact

If you believe anything here is wrong, say so and we will correct it in public with the date attached.

**John Bagshaw**, Founder, ShawSilicon Inc. Toronto, Ontario.
john@shawsilicon.ai | [shawsilicon.ai](https://shawsilicon.ai) | [github.com/taitashaw](https://github.com/taitashaw)

---

### Changelog
- **v0.1.2, 2 August 2026** -- corrected the screen description to three rounds and the bank to 300 items across the 9 selectable specializations. Earlier revisions said four stages and 380 items across 13; the extra 80 items belong to four specializations engineers cannot currently select.
- **v0.1, 2 August 2026** -- first publication. Outcome results n = 30, session funnel n = 22, round 1 n = 8. Round 2 flagged as unreliable pending investigation. Stages 3 and 4 not reportable.
