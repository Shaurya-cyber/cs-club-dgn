## DGN Computer Science Club — Official Website

The official club website for the **Downers Grove North High School Computer Science Club**. Built and maintained by student officers.

🌐 **Live Site:** *Pending — not yet published.*

**Disclaimer:** This site is created and maintained by club members. Content reflects the views of club members and has not been independently reviewed by school administration.

---

## About the Club

The DGN CS Club is a student-led organization open to all DGN students — no experience required. We meet twice a month (morning and afternoon sessions, same content) and run workshops, build projects, and host guest speakers.

- 📅 **Meetings:** 7:45–8:10 AM or 3:30–4:00 PM, twice a month
- 📍 **Location:** Room 308 (Mrs. Johnwick's room)
- ✉️ **Contact:** csclub.dgn@gmail.com

---

## What's on the Site

| Section | Description |
|---|---|
| Hero | Club tagline, beginner-friendly badge, quick stats, and call-to-action |
| About | Club overview, meeting info, core values, and a "typical meeting" breakdown |
| Try Coding | Interactive Python code demo with a simulated (animated, not live-executing) terminal, linked to an external CodeHS sandbox for real editing |
| Events | Schedule of meetings, guest speakers, and showcases — rendered dynamically from a JS data array, see [Updating Events](#updating-events) |
| Officers | Leadership team and roles |
| Join | Step-by-step instructions to become a member |
| Footer | Logo, disclaimer, Contact Us (email/Classroom/Infinite Campus), Quick Links, copyright |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (custom properties, CSS Grid, Flexbox) |
| Scripting | Vanilla JavaScript |
| Fonts | Google Fonts — Syne, Space Mono |
| Hosting | GitHub Pages *(pending setup)* |
| Code Editor | VS Code |

No frameworks. No dependencies. No build step — just open `index.html`.

---

## Project Structure

```
dgn-cs-club-website/
├── index.html                 # Main (and only) page — all sections live here
├── clublogotransparent.png    # Club logo used in nav and footer
├── LICENSE
└── README.md                  # You are here
```

---

## Updating Events

The Events section is rendered from a JavaScript array, not hardcoded HTML — this is the section that changes most often, so it's built to be edited in one place.

To add, remove, or update an event, edit the `events` array near the bottom of the `<script>` block in `index.html`:

```javascript
const events = [
  { date: "Sept 2", time: "7:45–8:10 AM", title: "Kickoff Meeting", desc: "...", badge: "upcoming" },
  // add more event objects here
];
```

**Field reference:**
- `date` — display date (use `"TBD"` if not yet confirmed by our sponsor)
- `time` *(optional)* — meeting/event time, shown under the date
- `title` — event name
- `desc` — one-sentence description
- `badge` — must be one of: `upcoming`, `recurring`, or `open` (these map to existing CSS badge styles — any other value renders unstyled)

Don't edit the HTML inside `.events-list` directly — it's populated automatically by `renderEvents()` on page load.

---

## Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/Shaurya-cyber/cs-club-dgn.git
   ```
2. Open `index.html` directly in any browser, **or** use the VS Code **Live Server** extension (right-click the file → "Open with Live Server") for auto-reload on save.

No server or install needed either way.

---

## Deployment

The site will be hosted on **GitHub Pages**. Deployment is currently pending setup.

Once configured, the recommended workflow is: make changes on a feature branch → test locally → open a pull request → merge to `master`.

---

## Git Workflow

The default branch is **`master`**.

**Before starting any change:**
```bash
git checkout master
git pull origin master
git checkout -b your-branch-name
```

**When ready to share your work:**
```bash
git add .
git commit -m "Clear, specific description of the change"
git push -u origin your-branch-name
```

Then open a pull request on GitHub so the other editor can review before merging into `master`.

Please write clear, specific commit messages — e.g. `Add spring hackathon to events` rather than `update`.

---

## Contributing

This repo is maintained by CS Club officers only — see [License](#license) below.

1. Create a new branch off `master`
2. Make your changes and test locally
3. Open a pull request with a short description of what you changed and why
4. Another officer reviews and merges

---

## Officers (2026–2027)

| Name | Role | Grade |
|---|---|---|
| Shaurya Shah | Co-President | 12th |
| Sarvesh Ganesh | Co-President | 11th |
| Leah Achilles | Co-President | 11th |
| Cristian Padinjath | Vice President | 11th |
| Rituraj Paul | Director of Operations | 10th |
| Ty Nguyen | Director of Development | 11th |

---

## Known Considerations

- The Try Coding terminal is a **scripted animation**, not a live code execution environment — a note under the terminal makes this clear to visitors. Real editing happens via the linked CodeHS sandbox.
- Event dates should stay as `"TBD"` until confirmed by our sponsor — avoid placeholder dates that could be mistaken for confirmed ones.
- Some footer links (Infinite Campus registration) may need updating if the district changes its portal URL.

---

## License

All rights reserved. This project — including its source code, design, and
content — is the property of the DGN Computer Science Club. No part of it
may be copied, modified, distributed, or reused without prior written
permission. For permission requests, contact csclub.dgn@gmail.com.

---

*© 2026–2027 DGN Computer Science Club — Downers Grove North High School*