# SF Community Input — HCS Outreach Dashboard

A static, self-contained dashboard summarising community input collected
by the SF Planning Department during Historic Context Statement (HCS)
outreach across San Francisco neighborhoods.

The dashboard answers one question:
**What does the public want preserved, and are certain communities'
voices stronger or weaker in this data?**

## Live page

The dashboard is published at the GitHub Pages URL of this repo.
Open `index.html` directly in any modern browser to use it offline.

## Sections

1. Overview — headline numbers
2. What people want preserved — by type
3. Cultural-group breakdown (tabbed)
4. Knowledge Bearers & high-priority items (sortable / filterable)
5. Outreach events — timeline
6. Gaps and questions — entries the community flagged as missing,
   lost, or at risk

## Data

The page is rendered from a sanitised snapshot of:

- `Community_Input.csv` — raw entries from outreach
- `Community_Input_Dashboard_-_Global.csv` — synthesised themes

The snapshot is **embedded inside `index.html`** as JSON.
Sensitive fields are stripped before publishing:

- the entire `SF Survey team response and/or action` column is dropped
- the raw `Notes` column is dropped, except that for entries the
  community flagged as missing/lost/at risk we keep a single ≤100-char
  redacted snippet (emails → `[email]`, phone numbers → `[phone]`)
  centred on the gap keyword

The neighbourhood CSVs themselves are **not** uploaded to this repo.
