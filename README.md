# Hi, I'm Bredan 👋

**Computer Science student at the University of Houston-Downtown (B.S., May 2028) who builds data pipelines, desktop apps, and search tools.**
Seeking **Summer 2027 software engineering internships** — open to relocating anywhere in the U.S.

[Portfolio](https://bredankm.dev) · [LinkedIn](https://www.linkedin.com/in/bredanmwaura/) · [Email](mailto:YOUR_EMAIL_HERE)

---

## Featured projects

### [Houston METRO Reliability Tracker](https://github.com/BreyKM/metro-reliability-tracker)
METRO's live feed shows where a bus is right now, but nothing shows whether it's usually late. This service records the feeds around the clock to build that history and answer: *what time should I leave to make it with 90% confidence?*

- Polls METRO's GTFS-Realtime arrival predictions and bus GPS feeds every 30 seconds, running 24/7 on a VPS — over 1M predictions across 106 routes and 8,900+ stops in its first three days, with zero missed polls
- PostgreSQL storage with forward-only upserts, so reprocessing old data can never overwrite newer data; every poll attempt is logged so any gap is visible and explained
- Production operations: Docker Compose, systemd services, nightly backups to Backblaze B2 with tested restores, and external monitoring that alerts when data stops arriving

`Python` `PostgreSQL` `Docker` `protobuf` `psycopg 3` `pytest` `GitHub Actions`

### [NovaNotes](https://github.com/BreyKM/NovaNotes)
A local-first markdown notes desktop app. It opens a folder of `.md` files and edits them in place, with live preview and no database.

- Built a custom CodeMirror 6 live-preview layer that renders markdown as you type without ever rewriting the file
- Made saving crash-safe: writes are queued so a slow save can't overtake a newer one, and each goes to a temp file before an atomic rename
- 213 Vitest tests, CI on every push, and architecture decision records documenting each major design choice

`TypeScript` `Electron` `Svelte 5` `CodeMirror 6` `Tailwind CSS` `Vitest`

### [numpy-vector-engine](https://github.com/BreyKM/numpy-vector-engine)
A semantic search engine built from scratch with NumPy. it finds a vacuum flask when you search "something to keep my coffee warm."

- Ranks 384-dimensional sentence embeddings by cosine similarity, reduced to a single matrix multiply by normalizing vectors at ingestion
- Selects top-k results in O(N) with `np.argpartition` instead of fully sorting every score
- pytest suite checks the optimized search against a direct implementation of the formula; Ruff and tests run in GitHub Actions

`Python` `NumPy` `sentence-transformers` `pytest` `GitHub Actions`

**Also built:** [PokePlex](https://github.com/BreyKM/pokePlex) — a React + Redux Toolkit Pokémon search app ([live demo](https://breykm.github.io/pokePlex/))

---

## Tech

**Languages:** Python, TypeScript, JavaScript, SQL, Java, C++  
**Backend & infrastructure:** PostgreSQL, Docker, Linux (systemd), GitHub Actions  
**Frontend & desktop:** React, Svelte, Electron, Tailwind CSS, HTML/CSS  
**Testing:** pytest, Vitest  
**Data:** NumPy, Pandas

## Currently

- Building a leave-by-time query and FastAPI service for the METRO tracker
- Member of the National Society of Black Engineers (NSBE)
- Sharpening data structures & algorithms in Python
