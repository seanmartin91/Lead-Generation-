# ITProspect — IT Business Development App

A single-file web app for IT account managers to discover, track, and close more business — with daily automated prospect discovery, a full call log with Teams/PBX integration, Hunter.io contact discovery, Google & LinkedIn smart links, and AI-powered outreach generation.

---

## Features

### Daily prospect discovery
- Save searches (city, industry, keyword) that run **automatically every time you open the app**
- New companies not seen before are flagged with a **"NEW TODAY"** badge and highlighted in blue
- A counter on the nav bar and metrics row shows how many new companies were found
- Delete or re-run individual searches at any time

### Call log & calling
- **Quick call** — pick any lead and dial via `tel:`, Microsoft Teams, or your PBX/VoIP system with one click
- **Teams integration** — click-to-call using the `msteams://` deep link protocol (opens Teams directly)
- **PBX / VoIP** — enter your system's URL scheme (e.g. `3cx:`, `rcmobile://`, `callto:`) and calls route through your PBX
- **Log calls** — record direction (outbound / inbound / missed), duration, notes, and schedule follow-up dates
- **Follow-ups auto-added** to reminders when you log a call with a follow-up date
- **Call back** button on every logged call
- Filter call log by: All / Outbound / Inbound / Missed
- **AI post-call follow-up** — generate a follow-up email or message from any call log entry

### Prospect search
- Describe what you're looking for in plain English ("law firms in Niagara Falls with 100 employees")
- AI parses city, industry, keyword, and size automatically (requires Anthropic key)
- Searches Hunter.io for verified email contacts
- Every company result includes one-click links: **Google**, **LinkedIn company**, **LinkedIn IT contacts**, **Google Maps**, **Google News**
- Each contact has a LinkedIn person search link
- **Save any search** to Daily Discovery from the search panel
- Export all results as **CSV**

### Lead management
- Add leads with phone, email, company, industry, size, and deal value
- Filter by size, industry, and pipeline status
- Phone icon on every lead with a phone number — click to open Quick Call
- AI outreach generator for each lead

### Pipeline view
- Kanban board: New → Contacted → Qualified → Proposal
- Deal value totals per column

### Reminders
- Colour-coded follow-up list (red = urgent, amber = soon, blue = upcoming)
- Auto-populated from call logs with follow-up dates

### Metrics dashboard
- Total leads, pipeline value, deals in progress, follow-ups due, **new today**

---

## Getting started

```bash
git clone https://github.com/YOUR_USERNAME/itprospect.git
cd itprospect
open index.html
```

No build step, no server, no dependencies.

### GitHub Pages (free hosting)

1. Go to your repo → **Settings** → **Pages**
2. Source: `main` branch, `/ (root)`
3. Save → live at `https://YOUR_USERNAME.github.io/itprospect/`

---

## API & integration setup

All keys are entered in the app's banners — never stored in code.

### Anthropic Claude (AI outreach + smart search parsing)
- Get a key at [console.anthropic.com](https://console.anthropic.com)
- Enables: AI outreach generation, post-call follow-ups, natural language search parsing

### Hunter.io (email contact discovery)
- Sign up at [hunter.io](https://hunter.io) — free plan: 25 searches/month
- Go to **Dashboard → API** to copy your key
- Enables: email contacts in search results and daily discovery

### Microsoft Teams (click-to-call)
- No setup required — uses the `msteams://` deep link protocol
- Requires Teams to be installed on your computer
- Click "Teams" on any Quick Call screen to open a call in Teams

### PBX / VoIP integration
- Enter your system's URL scheme in the purple banner (e.g. `3cx:`, `rcmobile://`, `callto:`, `sip:`)
- **3CX**: `3cx:`
- **RingCentral**: `rcmobile://`
- **Cisco**: `sip:`
- **Generic VoIP**: `callto:`
- Once set, a "PBX" button appears alongside Teams on every Quick Call screen

---

## Usage

| Feature | How to use |
|---|---|
| Daily discovery | Click **Daily discovery** → Save search → Run all now |
| Auto-run on open | Saved searches run automatically 0.8s after the page loads |
| Quick call | Click &#128222; on any lead → choose tel: / Teams / PBX |
| Log a call | Calls tab → Log call (or use Quick Call which auto-logs) |
| Post-call outreach | Calls tab → click Outreach on any logged call |
| Find prospects | Click **Search** → describe or filter → Find prospects |
| Save a search | Search tab → set filters → click Save search |
| Import contact | Click + Lead on any Hunter.io result |
| Generate outreach | Outreach ↗ on any lead |
| Export results | Export CSV in search results header |

---

## Tech stack

- Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools
- [Hunter.io API](https://hunter.io/api) — email discovery
- [Anthropic Claude API](https://www.anthropic.com/api) — AI outreach & parsing
- Microsoft Teams deep links (`msteams://`) — click-to-call
- PBX/VoIP URL schemes — configurable
- Google Search, Google Maps, Google News, LinkedIn — smart pre-filled URLs
- Google Fonts (DM Sans)
- Browser `localStorage` — persists call log, saved searches, seen domains, and API keys

---

## Licence

MIT — free to use, modify, and distribute.
