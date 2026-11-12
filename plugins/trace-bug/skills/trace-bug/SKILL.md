---
name: trace-bug
description: Diagnose a reproducible failure by comparing competing hypotheses against evidence.
---

1. Record the expected result, actual result, environment, and smallest known reproduction.
2. Identify the first boundary where behavior diverges. Use existing logs, tests or read-only inspection before adding instrumentation.
3. List plausible causes and pick a low-cost observation that distinguishes them. Record what each observation rules in or out.
4. Report the most specific supported cause, the evidence and a way to verify a fix. If evidence is incomplete, state the next experiment.
