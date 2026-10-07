# 🛡️ Kavach

> Turning the phone already charging on your nightstand into an early-warning system for the building around it.

**Kavach** (कवच, "shield") is a crowdsourced structural-health-monitoring system for India.

![Status](https://img.shields.io/badge/status-early%20development-yellow)

## The problem

Over half of India's population lives in moderate-to-high seismic hazard zones. The buildings most exposed to that risk — older, informal, self-built housing — are also the least likely to ever get a professional structural survey, since a formal inspection costs lakhs of rupees. In practice, problems are usually found only after a crack is already visible, or after a disaster.

## The idea

Every modern smartphone already carries an accelerometer sensitive enough to pick up a building's natural vibration. Kavach uses that: while a phone charges overnight, it quietly records the building's vibration "fingerprint." Collected across many phones and many nights, this builds a baseline for a structure — and the system watches for drift, a gradual or sudden shift that signals weakening. The output is a risk-ranked map that local disaster-management authorities can use to prioritize which buildings actually need an inspection, instead of waiting for a complaint.

No new hardware, no cost to the user — just a phone that was going to be charging there anyway.

This builds on real, peer-reviewed precedent: UC Berkeley's [MyShake](https://myshake.berkeley.edu/) project already showed phones can extract a building's fundamental frequency accurately enough to track structural health over time. Kavach adapts that specifically for India's largely non-engineered building stock, and for how Indian disaster-management authorities actually work.

## Status

🟡 **Early development — Phase I.** Learning core skills and validating the idea with real disaster-management contacts. No working build yet. Research notes and meeting logs are tracked separately in our team Notion workspace.

## Team

Anushka · Anuj · Naman

| Role | Owner |
|---|---|
| 📱 Mobile & Sensing | Anuj |
| 🧠 Data & Brain | Anushka |
| 🗺️ Dashboard & Outreach | Naman |

## Tech stack

| Layer | Stack |
|---|---|
| Mobile & Sensing | Kotlin, Android Sensor API |
| Data & Brain | Python, NumPy/SciPy, FastAPI/Flask, SQLite → PostgreSQL |
| Dashboard & Outreach | HTML, CSS, JavaScript, Leaflet.js |

## Repository structure

```
kavach/
├── mobile/      # Android app — sensing & on-device processing
├── backend/     # Signal processing, anomaly detection, API
├── dashboard/   # Authority-facing map & dashboard
├── docs/        # Diagrams, write-ups, exported research
└── README.md
```

## Roadmap

- [ ] **Phase I — Learn & validate** *(current)* — core skills, science, stakeholder conversations
- [ ] **Phase II — Build the first working version** — phone senses vibration → fingerprint extracted → basic dashboard
- [ ] **Phase III — Make it solid** — background sensing, real backend, tested on 5+ buildings
- [ ] **Phase IV — Test with real people** — pilot with real users on real phones

## Acknowledgments

- [MyShake](https://myshake.berkeley.edu/), UC Berkeley — the research precedent this idea builds on
- Samsung Solve for Tomorrow 2026

## License

TBD
