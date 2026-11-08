# First Response - Cyber

The doctrine pack. CISA's Federal Incident & Vulnerability Response Playbooks and NIST SP 800-61 Rev. 3 — incident lifecycle, containment, eradication, recovery, and vulnerability prioritization. What Navi answers from when things go wrong

A **knowledge pack** for Apex — Navi's answers can draw on
these documents, and cite the pack and document they came from.
The pack format is `navi-rag/1` (see `navi-rag.json`).

## Documents

- `documents/CISA_IR.txt`
- `documents/NISTSP800.txt`

## Install it in Navi

1. Open Navi's **RAG** tab, then **Packs**.
2. **Search GitHub** — every public repo tagged `navi-rag` is listed.
3. **Install** this pack. Navi downloads the documents at the latest
   release and builds the pack's index on your machine from them.

Only **active** packs feed her answers; toggle the pack off in the
same tab whenever you like.

## Layout

- `README.md` — this page. Navi's installer skips a root README, so
  it describes the pack without ever being indexed as a document.
- `navi-rag.json` — the pack manifest (name, version, document list).
- `index.json` — the pack's built index, shipped as a reference copy;
  installing Navi rebuilds it locally from the documents.
- `documents/` — the pack's documents (`.md` / `.txt`).

## Publishing an update

Edit the documents, bump `version` in `navi-rag.json`, push, and cut
a new release whose tag is the new version (this export is `0.1.0`). A newer release tag is what offers everyone who
installed the pack an update. Keep the `navi-rag` topic on the
repo — that is how Navi finds it.
