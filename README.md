# Harish Seshadri — @hseshadr

I build open-source, **local-first** systems for search, ranking, recommendations, and
transparent domain computation — where the critical work runs on your own device, data ships
as **signed bundles**, and results are **explainable**.

## Open-source projects

### EdgeReco — search & recommendations that run on the shopper's device

After a one-time sync of a signed catalog bundle, EdgeReco runs **BM25 keyword search, vector
search, reciprocal rank fusion (RRF), and session-aware reranking** entirely in the browser —
with no per-query backend call.

- 🔗 Live demo: **https://edge-reco.com**
- 📦 GitHub: **https://github.com/hseshadr/edge-reco**
- 🛒 Demo store: **Nimbus** — a fictional storefront used only to show the engine.

### EdgeProc — the local-first substrate EdgeReco is built on

EdgeProc (also written `edge-proc`) ships search/ranking indexes as **signed, content-addressed
bundles** (Ed25519 + SHA-256), **verifies them fail-closed**, and routes typed `SEARCH` /
`EMBED` / `RANK` tasks to a local FAISS runtime — no cloud in the query path. *Not affiliated
with any other product or company named "EdgeProc."*

- 📦 GitHub: **https://github.com/hseshadr/edge-proc**

## The common pattern

```txt
data bundle  →  local verification  →  domain engine  →  explainable result
```

Interests: browser-side compute, local-first AI, signed data bundles, on-device search &
vector retrieval, privacy-preserving recommendations, and transparent domain engines.
