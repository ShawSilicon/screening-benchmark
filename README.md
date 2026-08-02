# Chip design screening: methodology and first results

**ShawSilicon. Data cut 2 August 2026. Report version 0.1.**

Nobody publishes pass and fail rates for semiconductor technical screening. Recruiters do not measure it, employers do not release it, and assessment vendors have no reason to tell you how many people fail. So there is no public baseline for what a real chip design screen filters out.

This report is the beginning of one. It is deliberately small and deliberately honest about what it cannot yet say.

---

## What this report is, and is not

**It is** an outcome-level result at n = 30, a session funnel at n = 22, and a full description of the instrument that produced them.

**It is not** a benchmark. A benchmark needs enough observations to be stable, and this does not have them yet. Everything below carries its n. Nothing is extrapolated, and no percentage appears without the count behind it.

**It does not report per-stage failure rates.** We can measure them and we intend to publish them, but the sample is currently one to nine observations per stage depending on the stage, which is not enough to report. Section 5 states exactly how thin, because a report that hides its own gaps is the thing this company exists to argue against.

---

## 1. The instrument

Engineers complete four stages in their own specialization.

| Stage | What it tests | Scored dimension |
|---|---|---|
| 1 | Conceptual depth in the specialization | `conceptual_depth` |
| 2 | Applied work sample, code and written reasoning | `design`, `debugging` |
| 3 | A design diagram the candidate draws | `diagrams` |
| 4 | Live defense of that design under questioning, on camera | `adversarial_debug` |

Five scored dimensions in total. Stages 1 and 2 combine deterministic checks with model-assisted scoring. Stage 4 is graded by a practising FPGA engineer.

Question bank: **380 items across 13 specializations** (FPGA design, ASIC design, verification and UVM, formal verification, physical design, analog and mixed-signal, embedded hardware, AI chip architecture, DFT, quantum, HFT, defence, aerospace).

**Pass floor: 51 of 100.**

The rubric weights and the question bank are not published. The stage structure, the dimensions and the floor are.

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

Twenty-two sessions have been started on the four-stage flow.

| | Count |
|---|---|
| Sessions started | **22** |
| Submitted both stage 1 and stage 2 | **9** |
| Abandoned before submitting anything | **13** |
| Graded through all four stages | **1** |

**Thirteen of twenty-two starts produce no submission at all.** Those candidates opened the screen and left without answering. This is not a pass or fail result, and it is not counted as either, but it is the largest single number in the funnel and we would rather publish it than quietly drop it.

---

## 4. Stage 1 results, n = 8

The only stage with enough observations to show anything.

`conceptual_depth`, eight scored submissions: **63, 67, 77, 80, 80, 82, 83, 86**

Median 80. Range 63 to 86. This says the population reaching stage 1 submission is reasonably strong on fundamentals, which is expected: the drop-off in section 3 happens earlier.

Eight observations. Do not build anything on this.

---

## 5. What we cannot report yet, and how thin it is

| Stage | Dimension | Observations |
|---|---|---|
| 1 | `conceptual_depth` | 8 |
| 2 | `design` | 9 |
| 2 | `debugging` | 9 |
| 3 | `diagrams` | **1** |
| 4 | `adversarial_debug` | **1** |

Stages 3 and 4 have a single observation each. There is no per-stage failure rate to report and there will not be one until the sample supports it.

**One further disclosure.** In the stage 2 data, seven of nine `design` scores and seven of nine `debugging` scores are identical values. That pattern is more consistent with a scorer returning a default than with a scorer discriminating between candidates. Until that is investigated and resolved, **no stage 2 result should be treated as a measurement**, and none is reported above beyond the raw count. We are stating this rather than publishing a mean that looks meaningful and is not.

---

## 6. Method notes and limitations

- **Selection.** Candidates self-select by registering. This is not a random sample of chip engineers and should not be read as one.
- **Internal accounts excluded.** Company-domain and test accounts are removed from every figure above. Thirty-three scored records exist in total; three are internal and are excluded, leaving 30.
- **Two scoring generations.** The 30 outcome results span an earlier scoring flow and the current four-stage flow. The 51 floor applies to both. Per-stage data exists only for the current flow, which is why sections 2 and 4 have different n.
- **No placement outcomes.** We cannot yet report whether a passing score predicts on-the-job performance, because no engineer verified here has been placed. Predictive validity is the number that would matter most and we do not have it. Anyone claiming otherwise on this small a sample would be doing the thing this company exists to stop.

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
- **v0.1, 2 August 2026** -- first publication. Outcome results n = 30, session funnel n = 22, stage 1 n = 8. Stage 2 flagged as unreliable pending investigation. Stages 3 and 4 not reportable.
