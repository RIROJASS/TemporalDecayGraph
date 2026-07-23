# TemporalDecayGraph

A real-time EEG coherence graph where connections fade unless the brain keeps them alive. Electrode pairs are edges in a graph; each edge's weight (coherence across the Delta, Theta, Alpha, Beta, and Gamma bands) decays exponentially over time and is refreshed as new EEG data streams in. The result: a live head-map animation showing which brain regions are talking to each other *right now*, with stale connections dissolving on their own — no cleanup passes needed.

## How It Works

```mermaid
flowchart TD
    E[EEG stream<br/>21 electrodes, 10-20 system] --> I[TDG.in