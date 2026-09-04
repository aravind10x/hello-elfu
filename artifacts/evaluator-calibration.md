# Historical Evaluator Calibration

This is a public-safe summary of a seeded-defect acceptance exercise run on July 11, 2026. It evaluates the **evaluation harness**, not Elfu's product quality.

## Question being tested

If a known failure is deliberately introduced into a live audiovisual session, does the model-based judge return the expected structured finding at high severity and sufficient confidence?

The protocol distinguishes three outcomes:

- **Proven:** usable evidence contains the defect and the judge returns the required classification.
- **Blind spot:** usable evidence contains the defect but the judge misses the required classification.
- **Confounded:** the run, recorder, lifecycle, or injected stimulus is not reliable enough to evaluate the judge.

## Historical result

| Seeded defect | Expected finding | Result |
| --- | --- | --- |
| Repeated fallback loop | `repeated_fallback` | Proven |
| Topic or theme drift | `topic_theme_drift` | Confounded |
| Duplicate audio or turn | `duplicate_audio_or_turn` | Confounded |
| Injected latency | `latency` | Blind spot |
| Audio/visual desynchronization | `audio_visual_desync` | Confounded |

The exercise demonstrated one classification out of five. The latency run produced usable enough evidence to document a judge blind spot. Three other categories were confounded by mechanical failures or missing stimulus evidence and were not interpreted as judge passes or failures.

## Why publish an imperfect result

The result prevented the project from treating a multimodal model judge as a universal quality oracle. It led to a health-first evaluation policy:

1. reject instrument-unhealthy runs;
2. use deterministic monitors where the failure has a direct definition;
3. use model judging as an additional observer for qualitative behavior;
4. state blind spots and confounded evidence explicitly;
5. avoid collapsing a live child-facing system into one score.

The protocol and harness evolved after this historical snapshot. This artifact is retained as evidence of calibration discipline, not presented as the latest acceptance result.

## Important caveats

- Two baseline runs and one primary run per defect make the sample small.
- The judge was a single model rather than a consensus panel.
- Integer diagnostic scores were too coarse to serve as the trust criterion.
- Network, session lifecycle, recording, and injection failures can all confound live evaluation.
- A judge's ability to detect an injected defect says nothing by itself about the overall safety or quality of Elfu.

