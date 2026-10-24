# LaneTrace footprint studio

A visual contention explorer, built around a conflict graph, pairwise access matrix, illustrative lane rows and an evidence inspector. Open the teaching trace or capture current testnet footprints. Switch between shared aggregate, isolated slots, reader-only and all-call workloads. Select a pair to inspect the precise write/read or write/write key; select a hotspot to see its readers and writers.

The selected lane count is an educational parameter, not a fetched network setting. Instruction resources are not measured durations. The shared and isolated workloads deliberately implement different aggregate semantics, disclosed beside the visualization.

Run the sibling API on 4401, then `node server.mjs` here and visit http://127.0.0.1:4400. Imports accept a public trace or the exported `{trace,report}` bundle; imported labels are rendered as text. No JSON editor, signing or wallet flow. Self-only CSP and loopback proxy. `node --test test.mjs` checks served controls and scope disclosures. Keyboard graph alternatives are provided through transaction buttons and pairwise matrix cells.

## Protocol reference

[CAP-0063](https://github.com/stellar/stellar-protocol/blob/master/core/cap-0063.md) defines the footprint conflict rule and staged cluster semantics. LaneTrace implements the declared-key conflict rule and an illustrative clustering model only.
