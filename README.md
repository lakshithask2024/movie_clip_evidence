# YouTube Risk Report

This project is a Python notebook (`.ipynb`) that pulls YouTube video/channel data, computes risk signals, and generates a structured Excel report for review.

---

## What this notebook does

Given a list of YouTube channels/handles (or a query), the notebook:
1. Collects channel + video metadata (title, description, publish date, stats, URL, etc.)

2. Applies a risk-signal analysis to produce:
   - `risk_score`
   - `risk_label`
   - `risk_signals` / `red_flags` / `evidence_summary`
3. Exports everything into a timestamped Excel report.

---

## Output files

After running the notebook, you should get:

- **Excel Report**
  - Example: `report_YYYYMMDD_HHMMSS.xlsx`
  - One row per video with columns like:
    - `channel_name`, `channel_id`, `video_id`, `video_url`
    - `title`, `description`, `published_at`
    - `views`, `likes`, `comments`, `duration_seconds`
    - `risk_score`, `risk_label`, `risk_signals`, `evidence_summary`
    - `evidence_path` (if evidence saving is enabled)

- **Evidence folder**
  - Example: `evidence/run_YYYYMMDD_HHMMSS/`
  - Contains any saved supporting artifacts (screenshots, JSON dumps, logs, etc.)

- **Manifest file**
  - Example: `manifest.json`
  - Stores what was pulled and what was generated, for traceability.



## Requirements

- Python: 3.9+ (recommended)
- Install dependencies

---

## This notebook is designed to use free services only
  If you are using the YouTube Data API:
- Create a free API key in Google Cloud Console
- paste into the notebook config cell
- YOUTUBE_API_KEY=YOUR_KEY_HERE

```bash


