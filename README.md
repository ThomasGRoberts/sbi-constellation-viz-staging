# Space-Based Interceptors and Strategic Stability

An interactive Engineering Space Policy Laboratory visualization of space-based interceptor constellations for four threat regions.

## Preview

Serve this directory over HTTP, then open the local URL in a browser:

```sh
python3 -m http.server 8877
```

Open <http://localhost:8877/>. The application loads JavaScript libraries from CDNs, so an internet connection is needed.

## Data

This staging copy includes the CSV and JSON result files referenced by all 140 available Principal Runs. The chart and coverage calculations use the full simulation rows. Grouped orbital trajectories and their aligned satellite sprites are a 3D display approximation. When a run enables J2, the displayed trajectories precess at the analytical J2 rate. Satellite sprites are projected onto those trajectories, and Earth rotation follows simulation time.
