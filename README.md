# WeightTraining

A bare-bones, no-frills personal tracker. Three things, no accounts, no subscriptions, no notifications begging for attention.

- **LIFT** — checklist for a simple 2-workout home strength program (Workouts A and B), tracks sessions per week
- **FAST** — intermittent fasting timer with configurable goal
- **WEIGH** — daily weight entry with 7-day moving average trend chart

All data lives in your browser's localStorage. Nothing is sent anywhere.

## Use it on your phone

### Option 1: GitHub Pages (recommended)

1. Create a new public repo on GitHub (call it whatever — `log`, `tracker`, etc.)
2. Drop `index.html` into the root of the repo
3. Go to **Settings → Pages**, set source to `main` branch, root folder, save
4. Wait ~1 minute, then open `https://<your-username>.github.io/<repo-name>/` on your phone
5. In Safari/Chrome, tap the share icon → **Add to Home Screen**

Now it lives on your home screen like an app.

### Option 2: Just open the file

You can also just download `index.html` and open it locally in any browser. Data still saves. Less convenient on phone.

## Workout program

**Workout A** — Push / Squat / Core
- Goblet Squat to Chair — 3 × 10
- Push-Ups — 3 × max-1
- Single-Arm DB Row — 3 × 10 / side
- Glute Bridge / Hip Thrust — 3 × 15
- Plank — 3 × 30–45s

**Workout B** — Hinge / Pull / Core
- Romanian Deadlift (DB) — 3 × 10
- Reverse Lunge — 3 × 8 / side
- Overhead Press (DB) — 3 × 8–10
- Dead Bug — 3 × 10 / side
- Side Plank — 3 × 20–30s / side

Alternate A and B. Aim for 2 sessions per week.

## Want reminders?

This app has none on purpose. For nudges, set up recurring reminders in your phone's built-in Reminders or Calendar app:
- Mon/Thu 7pm → "Lift"
- After dinner → "Start fast"
- 7am daily → "Weigh in"

Tapping the reminder can deep-link to the app if you used Add to Home Screen.

## Customize

To change the workouts, find the `PROGRAM` constant near the top of the `<script>` tag in `index.html` and edit. To change the weekly session target, edit `WEEK_GOAL`.

## Data

- Storage: localStorage, keys are `sessions`, `fast`, `weights`, `activeWorkout`, `lastTab`, `weightRange`
- To backup: open browser DevTools → Application → Local Storage → copy out
- To wipe: clear site data in browser settings
