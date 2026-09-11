# Source Edit Overreach

## Symptom
A local source edit changes the voice, tempo, key, arrangement, or unrelated lyrics; source-based output keeps noise instead of the useful layer.

## Likely cause
The prompt asks to preserve and replace too many things at once, or the source timestamp contains multiple candidate elements.

## Conservative repair
Narrow the timestamp, choose one target element, and state one preservation priority. List every element that must remain unchanged.

## Exploratory repair
Use `v6-wild` to reinterpret one isolated layer, then return to `v6` with a strict rebuild instruction and original supporting parts.
