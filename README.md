# VERITAS-IAD Reviewer Simulation

Interactive multi-screen industrial inspection simulation generated from the frozen VERITAS-IAD design and accepted experiment artifacts.

- **Live simulation:** https://pratikpatelresearch.github.io/VERITAS-IAD-simulation/
- **Main implementation:** https://github.com/pratikpatelresearch/VERITAS-IAD

Reviewers can select frozen industrial scenarios, observe the five-agent workflow, inspect anomaly evidence, explore calibration and selective-risk results, export a decision trace, and use the blinded-rating interface. The application runs entirely in the browser and requires no API key or backend.

## Run locally

```bash
python3 -m http.server 4173 --directory deployment-and-human-evaluation
```

Open `http://127.0.0.1:4173`.

## Application workflow

Use the sidebar to move between Overview, New Inspection, Decision Review, Evidence Explorer, Operations, and Human Evaluation. New Inspection supports three deterministic industrial scenarios and local image preview. Running an inspection animates the five-agent pipeline, creates a session-history record, and opens the evidence-backed Decision Review.

## Evidence boundaries

- This is an interactive reviewer simulation using frozen representative outputs, not live model inference.
- A locally selected image is previewed in the browser and is not uploaded; the simulated result continues to follow the selected frozen scenario.
- Numerical values come from accepted Drive artifacts and `PROJECT_HANDOFF.md`.
- The human-rating interface stores illustrative assessments in browser `localStorage`.
- All visible quantitative results trace to accepted implementation evidence.
- Six full-screen application screenshots are stored under `screenshots/` after browser QA.
- `PAPER_FIGURE_GUIDE.md` maps each capture to a defensible caption and claim boundary.
- `data/human_evaluation_sample.csv` is an illustrative blank schema, not collected research data.

## Privacy

The site has no server-side component, analytics, account system, or data-upload endpoint. Browser-local previews, session history, ratings, and exported traces remain on the reviewer's device.
