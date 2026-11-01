# Comment log implementation — November 1, 2026

Source: [published team comment log](https://docs.google.com/spreadsheets/d/e/2PACX-1vSP5u6SAb1XyIguS6Z5omNhc3uXXvKKWqUqYBztBIvYG8kgBLqG43gLwABOR334IZJJPH1RTIC1jaiI/pubhtml). Row numbers are the sheet row numbers, including its header. The team controls the sheet's resolution status; this file records the staging implementation only.

| Row | Staging implementation |
| --- | --- |
| 2 | Highlighted 3D satellites are selected from displayed dot positions relative to the displayed Earth; the dynamic chart still uses the solver's full analytical orbits. |
| 3 | Returning from the dormant carousel resumes simulation immediately; the globe and constellation keep moving on the inertial timeline throughout the camera return. |
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
| 18 | Configuring satellite dots have bordered cores matching the 3D legend. The chart axes stay visible during configuration and its series waits for population to finish. |
| 19 | Playback controls and chart wait until the constellation reveal finishes. |
| 20 | Initial load runs the full North Korea outline, launch-site, and satellite population sequence from a North Korea camera focus. |
| 21 | Glossary terms refresh from the live published sheet on each page load; the bundled snapshot is a fallback and was refreshed. |
| 22 | Tested 50,000 tessellation cells. At that density, the 21,986-satellite China run had 133 ms frame gaps even after coverage optimization, and an ordinary 2,116-satellite run had 66 ms gaps. The retained desktop density is 25,000 cells for constellations with at most 10,000 satellites; larger solutions and phone screens use 15,000. Coverage lookup uses a numeric spatial index and scalar visibility math; map colors are cached per count, and projection transitions sample at most 8,000 cells. |
| 23 | The 2D zoom-in button morphs to the regional view and reveals sites without fading out coverage or rerunning the intro. |
| 7 | Added a portrait phone layout with a cropped, tilted globe, a scrollable lower control panel, a compact playback dock, and view controls at upper right. |

Browser checks covered the prior round's Iran salvo choices, rapid scenario switching, bidirectional chart scrubbing, carousel round trip, and the China 100-missile, 21,986-satellite run at 12 hours. This round checked the North Korea introduction, live glossary, chart waiting state, global and regional 2D views, 50,000-cell draw cost, and portrait phone framing. The catalog's `sourceGeneratedUtc` records the Drive snapshot used in this staging copy. Later Drive additions require another refresh and push.
