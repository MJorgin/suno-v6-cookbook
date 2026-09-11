# Wrong Model Choice

## Symptom
A controlled edit changes the whole song, a quick idea sounds too conventional, or a polished request drifts unpredictably.

## Likely cause
The model route does not match the task: precision requires `v6`, cheap drafts suit `v6-mini`, and open exploration suits `v6-wild`.

## Conservative repair
Switch local edits and polished text-to-song tasks to `v6`; simplify the instruction and explicitly list what must remain.

## Exploratory repair
Use `v6-wild` only for a bounded question, such as a bridge or texture idea, then pass one chosen result to `v6`.
