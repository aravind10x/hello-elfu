# Sanitized Robo-Kid Sample Run

This directory contains aggregate evidence from one live Robo-Kid session recorded on August 29, 2026.

## Scenario

- **Topic:** trains
- **Activity:** story
- **Persona:** cooperative, high attention, no planned interruptions
- **Expected ending:** the child says goodbye and Elfu reaches parent handoff

## Outcome

| Measure | Observed |
| --- | ---: |
| Duration | 2 min 31 sec |
| Elfu turns | 12 |
| Robo-Kid turns | 4 |
| Completed exchanges | 4 |
| Mean child-to-first-scheduled-audio latency | 1.94 sec |
| Minimum / maximum latency | 1.40 / 2.30 sec |
| Final scene | `parent_handoff` |
| Completed | yes |
| Instrument-health checks | 11 passed |
| Aggregate monitor findings | none |

## Files

- [`scenario.yaml`](scenario.yaml): the sanitized scenario card.
- [`summary.json`](summary.json): aggregate session and timing data.
- [`instrument-health.json`](instrument-health.json): checks used to determine whether the recording is usable evidence.
- [`run-report.json`](run-report.json): aggregate health and monitor result.

## What is omitted

The original run also produced synchronized video, separate and mixed audio, a raw event stream, and a snapshot of the product's turn records. Those files can contain child-facing dialogue and internal implementation details and are not published here.

This is evidence about one cooperative session, not a representative benchmark or a claim of safety.
