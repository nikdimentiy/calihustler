# California Hustler

A web-based daily mission tracker and habit-building application built to foster productivity, discipline, and long-term personal growth. Features a cyberpunk-inspired dark UI with neon accents, combining gamification, data visualization, and Supabase cloud sync.

> "Build your future, break bad habits, leave a legacy."

## Features

### Daily Missions

10 weighted missions spanning key life areas:

| Mission | Category | Weight |
| --- | --- | --- |
| Time Mastery | Productivity | 3 |
| Intellectual Feast | Knowledge | 2 |
| Virtue Cultivator | Character | 2 |
| Energy Recovery | Health | 3 |
| Learn Core | Tech/Learning | 2 |
| Global Voice | Language | 2 |
| Conclusion Journal | Mindset | 1 |
| Sculpted Physique | Fitness | 3 |
| Financial Fortress | Finance | 2 |
| Prime Day Launch | Routine | 3 |

### Metrics Dashboard

- Current & best streaks
- 7-day and monthly averages
- Weighted hustle score
- Perfect days count
- 14-day per-mission completion rates
- Weekday weakness detection
- Month-over-month comparisons

### Visualizations

- **30-Day Activity Heatmap** — daily activity intensity at a glance
- **Interactive Mission Timeline** — clickable calendar with per-day breakdowns
- **Month Rail** — fixed right-side monthly progress indicator

### Cloud & Offline

- **Supabase Auth** — email/password authentication
- **Cloud Sync** — missions and logs synced to `daily_logs` and `missions` tables
- **Local Storage** — full offline functionality with automatic cache

### UX

- Responsive layout (desktop → mobile, breakpoints at 1100 / 700 / 599 / 480px)
- Dark cyberpunk theme — neon cyan, pink, gold, green, purple on deep blue (`#050810`)
- ARIA labels, keyboard navigation, screen reader support
- PWA-capable (standalone display mode)

## Tech Stack

- **Frontend:** Vanilla JS, HTML5, CSS3 — no framework, no build step
- **Cloud:** Supabase (PostgreSQL + Auth)
- **Fonts:** Rajdhani, Orbitron, Share Tech Mono (Google Fonts)
- **Icons:** Font Awesome 6.5.0
- **Deploy:** GitHub Pages via Actions

## Getting Started

### Prerequisites

- Any modern browser (Chrome, Firefox, Safari, Edge)
- Internet connection required only for cloud sync and auth

### Run Locally

```bash
git clone https://github.com/yourusername/california-hustler.git
cd california-hustler
open index.html   # or double-click — no build step needed
```

### Cloud Sync Setup

1. Create a free [Supabase](https://supabase.com) project.
2. Add your Supabase URL and anon key to the app config in `app.min.js` (or the source before minification).
3. Create two tables: `daily_logs` and `missions`.
4. Register via the in-app auth widget (top-left corner).

## Daily Workflow

1. **Morning** — review yesterday's results, set your energy level (Low / Medium / High).
2. **Throughout the day** — click missions as you complete them.
3. **Evening** — check streaks, heatmap, and plan tomorrow.
4. **Weekly** — aim for the Five2Five challenge (5 days × 5 hours deep work).

## Keyboard Shortcuts

| Action | Shortcut |
| --- | --- |
| Toggle mission complete | `Shift + Enter` or right-click |
| Navigate UI elements | `Tab` |

## Deployment

The repo deploys automatically to GitHub Pages on every push to `main` via the included Actions workflow (`.github/workflows/static.yml`).

## License

GNU General Public License v3 — see [LICENSE](LICENSE).
