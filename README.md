# Space-Based Interceptors and Strategic Stability

An interactive Engineering Space Policy Laboratory visualization of space-based interceptor constellations for four threat regions.

## Preview

Serve this directory over HTTP, then open the local URL in a browser:

```sh
python3 -m http.server 8877
```

Open <http://localhost:8877/>. The application loads JavaScript libraries from CDNs, so an internet connection is needed.

## Data

This staging copy includes the CSV and JSON result files for all 768 feasible Principal Runs in the four displayed regions from the Google Drive export whose generation time is recorded as `sourceGeneratedUtc` in `principal-panel-data.json`. It is a static snapshot: later Drive additions require rebuilding `principal-panel-data.json` from the current `principal_runs/index.json` and republishing the referenced result files. The catalog identifies 141 proven optimal results and 627 results with a feasible constellation saved when the solver reached its time limit. The control panel labels the latter with their optimality gap; their satellite counts are not proven minima.

The chart and coverage calculations use the full simulation rows. Grouped orbital trajectories and their aligned satellite sprites are a 3D display approximation. When a run enables J2, coverage and sprites use the J2 corrected along-orbit and nodal rates; displayed trajectories precess at the same nodal rate. Satellite sprites are projected onto those trajectories, and Earth rotation follows simulation time. The chart samples the run's discrete analysis time grid.
