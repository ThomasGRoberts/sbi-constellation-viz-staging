# Comment log implementation — November 1, 2026

Source: [published team comment log](https://docs.google.com/spreadsheets/d/e/2PACX-1vSP5u6SAb1XyIguS6Z5omNhc3uXXvKKWqUqYBztBIvYG8kgBLqG43gLwABOR334IZJJPH1RTIC1jaiI/pubhtml). Row numbers are the sheet row numbers, including its header. The team controls the sheet's resolution status; this file records the staging implementation only.

| Row | Staging implementation |
| --- | --- |
| 2 | Highlighted 3D satellites are selected from displayed dot positions relative to the displayed Earth; the dynamic chart still uses the solver's full analytical orbits. |
| 3 | Returning from the dormant carousel pauses simulation and changes camera framing without changing globe or constellation orientation. |
| 5 | Refreshed the catalog from the current Drive `principal_runs` index. All four-region salvo and advanced-setting permutations remain present: 768 runs total. |
| 8 | Launch-site labels refresh from the live Scenario Language sheet by geographic coordinates; result names remain a fallback. |
| 9 | Darkened national borders on the 2D map and both 3D presentation modes. |
| 10 | Launch-site gold and dark blips play once per reveal or color transition. |
| 11 | Globe borders use local 50m country data and straight surface-following segments, avoiding spline loops. |
| 12 | Removed the two technical-term header icons. |
| 13 | Collapsed advanced-configuration summary wraps instead of clipping. |
| 14 | Scrubbing reconstructs the complete recent chart window in either direction; playback ends at 12 hours. |
| 15 | Added a hover-responsive information cue to the selected scenario tile. |
| 16 | Selected launch sites in scenario details use the dot-and-blip motif; unselected sites keep their existing treatment. |
| 17 | Scenario detail opens for the selected tile even while its Principal Run is still loading. |
| 18 | The satellite-count placeholder animates gray dots through a gold center position. |
| 19 | Playback controls and chart wait until the constellation reveal finishes. |

Browser checks covered Iran's four salvo choices, rapid scenario switching, bidirectional chart scrubbing, a carousel round trip, and the China 100-missile, 21,986-satellite run at 12 hours. The catalog's `sourceGeneratedUtc` records the Drive snapshot used in this staging copy. Later Drive additions require another refresh and push.
