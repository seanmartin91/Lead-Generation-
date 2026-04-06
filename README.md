ITProspect — IT Business Development App

A lightweight, single-file web app built for IT account managers to discover, track, and close more business — with Hunter.io contact discovery, one-click Google & LinkedIn research links, and AI-powered outreach generation.

---

## Features

- **Prospect search** — Describe what you're looking for in plain English (e.g. "law firms in Niagara Falls") and the app finds matching companies
- **Google & LinkedIn smart links** — Every company result includes one-click links to Google, LinkedIn company page, LinkedIn IT contacts, Google Maps, and Google News — no extra setup needed
- **Hunter.io email discovery** — Search any company domain to find verified email contacts with confidence scores
- **One-click lead import** — Import any Hunter.io contact directly into your leads pipeline
- **Lead management** — Track prospects by company, contact, industry, size, deal value, and status
- **Pipeline view** — Kanban board across New → Contacted → Qualified → Proposal
- **Follow-up reminders** — Colour-coded task list (red = urgent, amber = soon, blue = upcoming)
- **AI outreach generator** — Generate personalised cold emails, follow-ups, LinkedIn messages, and meeting requests using Claude
- **CSV export** — Download all prospect search results as a spreadsheet
- **Live metrics dashboard** — Total leads, pipeline value, active deals, and follow-ups due

---

## Getting started

### Option 1 — Open directly in your browser

```bash
git clone https://github.com/YOUR_USERNAME/itprospect.git
cd itprospect
open index.html
```

No build step, no server, no dependencies required.

### Option 2 — Host on GitHub Pages (free, shareable URL)

1. Go to your repository → **Settings** → **Pages**
2. Set source to `main` branch, `/ (root)`
3. Click **Save** — live at `https://YOUR_USERNAME.github.io/itprospect/`

---

## API key setup

Two optional API keys unlock additional features. Both are entered in the app's banners — never stored in code.

### Anthropic Claude (AI outreach + smart search parsing)

1. Get a key at [console.anthropic.com](https://console.anthropic.com)
2. Paste into the yellow banner when you open the app
3. Enables: AI outreach generation + natural language search parsing (e.g. auto-extracts city/industry from "law firms in Niagara Falls")

### Hunter.io (email contact discovery)

1. Sign up at [hunter.io](https://hunter.io) — free plan includes 25 searches/month
2. Go to **Dashboard → API** to copy your key
3. Paste into the orange banner when you open the app
4. Enables: verified email contacts for each company found

> Both keys are stored only in your browser's local storage and are never committed to your repository.

---

## Google & LinkedIn search links

No API key needed — these work instantly for every company in your search results:

| Link | What it does |
|---|---|
| **Google** | Searches the company name + city + "IT services" |
| **LinkedIn company** | Finds the company's LinkedIn profile |
| **LinkedIn IT contacts** | Filters LinkedIn for IT Manager/Director roles at that company |
| **Google Maps** | Shows the company's physical location |
| **Google News** | Latest news about the company — useful for spotting expansion, funding, or leadership changes before you reach out |

Each individual contact also has a LinkedIn icon that searches for that specific person by name and company.

---

## Usage

| Feature | How to use |
|---|---|
| Search for prospects | Click **Find prospects** → type a description → hit Search |
| Research a company | Click Google, LinkedIn, Maps, or News links on any result card |
| Find email contacts | Expand "View contacts" on any result card (requires Hunter.io key) |
| Import a contact | Click **+ Lead** next to any contact → confirm details |
| Generate outreach | Click **Outreach ↗** on any lead → choose type → Generate with AI |
| Export results | Click **Export CSV** in the search results header |
| Add a lead manually | Click **+ Add lead** in the top right |
| Mark reminders done | Click **Done** in the Reminders tab |

---

## Tech stack

- Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools
- [Hunter.io API](https://hunter.io/api) for email contact discovery
- [Anthropic Claude API](https://www.anthropic.com/api) for AI outreach and search parsing
- Google Fonts (DM Sans)
- Google Search, Google Maps, Google News, and LinkedIn via smart pre-filled URLs (no API key required)

---

## Customisation

All sample data is in the `<script>` block at the bottom of `index.html`:

- **Edit sample leads** — modify the `leads` array
- **Edit reminders** — modify the `reminders` array
- **Add industries** — update the `<select>` dropdowns in the filters and modals
- **Persist data** — replace in-memory arrays with `localStorage` reads/writes

---

## Licence

MIT — free to use, modify, and distribute.
