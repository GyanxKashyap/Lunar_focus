# Lunar Focus 🌙

**Turn study time into a growing lunar orbit.**

Lunar Focus is a browser-based study dashboard that combines a focus timer, session planning, analytics, and a lunar reward system. Plan what you want to study, start a session, and watch the moon and its rings develop as you put in the time.

Built with vanilla HTML, CSS, and JavaScript. No account, backend, package installation, or build step is required.

## Features

- **Two timer modes:** a configurable Focus countdown and an open-ended Count Up timer, plus a separate break timer.
- **Session planning:** subjects, tags, notes, and a task checklist, with Quick Start for sessions without a task list.
- **Visual progress:** an animated moon and orbit rings respond to study time, pauses, recovery, and interrupted sessions.
- **Study analytics:** daily goals, weekly charts, subject summaries, mode comparisons, personal records, and a calendar heatmap.
- **Session history:** review completed and interrupted sessions and filter them by subject, tag, and date.
- **Rewards:** XP, ranks, streaks, daily quests, achievements, and Lunar Tokens for orbit styles, themes, and bundles.
- **Data portability:** export a JSON backup, restore a backup, or download session records as CSV.
- **Local persistence:** settings, progress, and session data are saved using browser `localStorage`.

## Run locally

With Git and Python 3 installed:

```bash
git clone https://github.com/GyanxKashyap/Lunar_focus.git
cd Lunar_focus
python3 -m http.server 8000 --bind 127.0.0.1
```

Open [localhost:8000](http://localhost:8000). Stop the server with `Ctrl+C`. Python only serves the static files; the application runs in your browser.

## Your first session

1. Complete or skip the welcome tutorial.
2. Add a subject and tasks, or choose **Quick** to start without planning.
3. Choose **Focus** or **Count Up** and set a duration for Focus mode.
4. Start studying. Use the session review to inspect the result and start a break.
5. Review your analytics and history, or visit the Orbit Store to spend earned tokens.

The optional Anti-Distraction Lock adds confirmation steps to pause/reset actions and counts tab departures during a running session. It does not block other applications or websites.

## Data and persistence

Data belongs to the browser profile and origin where you use the app; there is no cloud synchronization. Keep using the same local address and port to access the same records. Clearing site data removes local progress, so use the backup controls in Settings before switching browsers or clearing storage.

History is capped at the **100 most recent sessions**. Export regularly to retain a longer record. An imported backup replaces saved app state; imports are blocked while a timer session is active.

## Project structure

```text
Lunar_focus/
├── index.html                   # UI, styles, timers, analytics, and storage
├── assets/
│   └── lunar-focus-logo.svg      # Project logo
└── README.md
```

## Development

Edit `index.html` and refresh the browser. Styles and application logic are kept together in that file. Use a separate browser profile when experimenting with rewards, history, or backup imports.

There is no automated test suite. Useful manual checks include completing a short focus session, saving a count-up session, reloading to check persistence, and verifying JSON backup/restore and CSV export.

---

Created by [Gyan Kashyap](https://github.com/GyanxKashyap).
