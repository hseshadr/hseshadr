# Harish Seshadri

I build open-source software for decisions where "trust me" isn't good enough — the software
has to show its work. The computation runs **on your own device, in your browser**; data
doesn't leave it, and results can carry a cryptographic receipt anyone can check later.
Everything below is free to use and live today, and all published source is MIT-licensed.

## Why

Software increasingly makes calls that affect real people: whether a payment looks suspicious,
what your private text reveals, what you're shown next. Most of it runs on someone else's
server, where you can't see the data it used or check the answer it gave. I think those
decisions should be **inspectable** (the code is open), **private** (your data stays with
you), and **repeatable** (same input, same answer, every time). So each project here moves
the computation into your browser and makes the result something you can verify — not
something you have to take on faith.

## What's live

| Product | What it does | Try it | Source |
|---|---|---|---|
| **AlmaMesh** | A full Vedic astrology app: enter a birth date, time, and place and it computes the chart on your device, with a real astronomy engine running in the browser. Free, no account, works offline after first load. | [almamesh.com](https://almamesh.com) | [gainratio/almamesh](https://github.com/gainratio/almamesh) |
| **AML-Filter** | Sanctions-list screening — the "is this name on a watchlist?" check banks run — done entirely in your browser: fuzzy name matching over signed watchlists, with an explanation for every match. | [aml-filter.com](https://aml-filter.com) | [gainratio/aml-filter](https://github.com/gainratio/aml-filter) |
| **EdgeReco** | A store's search and "you might also like", running inside the shopper's browser tab — after a one-time catalog sync there are no per-query server calls. | [edge-reco.com](https://edge-reco.com) | [gainratio/edge-reco](https://github.com/gainratio/edge-reco) |

### Published packages

| Package | What it does | Get it |
|---|---|---|
| `edge-proc` (Python) | Publishes data or `.sqlite` databases as signed, content-addressed bundles and searches them offline. | [PyPI](https://pypi.org/project/edge-proc/) · [GitHub](https://github.com/gainratio/edge-proc) |
| `@gainratio/browser` (TypeScript) | Verifies and syncs `edge-proc` bundles in a browser Web Worker, with OPFS SQLite FTS5, JSON1, and vector search. | [npm](https://www.npmjs.com/package/@gainratio/browser) · [GitHub](https://github.com/gainratio/edgeproc-browser) |
| `edgeproc-core` (Python) | Multi-tenant vector-index partitioning protocol and canonical error catalog underneath `edge-proc` and `EdgeReco`. | [PyPI](https://pypi.org/project/edgeproc-core/) · [GitHub](https://github.com/gainratio/edgeproc-core) |
| `avow` (Python) | Signed, offline-verifiable receipts: wrap a result in an envelope anyone can later check for tampering using only a public key. | [PyPI](https://pypi.org/project/avow/) · [GitHub](https://github.com/gainratio/avow) |
| `@gainratio/avow` (TypeScript) | The browser side of the same receipts — byte-for-byte compatible with the Python version, proven by a shared test suite. | [npm](https://www.npmjs.com/package/@gainratio/avow) · [GitHub](https://github.com/gainratio/avow) |
| `@gainratio/privacy-core` (TypeScript) | Redacts private text on your device before it reaches an AI model, then restores the real values locally in the reply — sending raw text is a compile error, not a policy. | [npm](https://www.npmjs.com/package/@gainratio/privacy-core) · [GitHub](https://github.com/gainratio/privacy-core) |
| `@gainratio/errors` (TypeScript) | Typed error registry with RFC 9457 Problem Details and i18n, matching `edgeproc-core` error codes. | [npm](https://www.npmjs.com/package/@gainratio/errors) · [GitHub](https://github.com/gainratio/errors) |
| `assay-engine` (Python) | Offline evaluation harness for ranking and retrieval quality gates. | [PyPI](https://pypi.org/project/assay-engine/) · [GitHub](https://github.com/gainratio/assay) |

### Under the hood (source)

- [gainratio](https://github.com/gainratio) — the organization hosting all public source repositories, shared Dagger CI modules ([gainratio/ci](https://github.com/gainratio/ci)), and release workflows.

## How I build

- **Runs in your browser.** The interesting computation happens on your device; your data doesn't leave it.
- **Deterministic.** Same input, same answer, every time — no hidden randomness in the core engines.
- **Verifiable.** Data ships signed and is checked before use; results can carry signed receipts that can be audited later, offline.
- **Honest about limits.** Every project states what it can't promise as plainly as what it can.
- **Tested before shipped.** Behavior is pinned by automated tests that run on every change, including cross-language compatibility suites.
- **Reproducible from clone.** Each repo has a quickstart that takes you from `git clone` to working output.

## About

Harish Seshadri — Senior Principal Engineer (AI/ML) at Gap Inc. This is my open-source
work, built in public. Reach me here on GitHub, or through any of the sites above.

---

All source repositories and packages linked above are MIT-licensed. The products are free,
need no account, and their pages load no third-party tracking scripts.
