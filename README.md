# 🏋️ Personal Multi-Sport Fitness Tracker — Excel Workbook

> **Self-built Excel fitness tracker** covering 8 activity types — Gym, Workout, Run, Walk, Swim, Cycle, Tennis, and Sauna recovery — with MET-based calorie calculations, performance records, RPE tracking, and a fully automated Daily Analysis dashboard. Fill in the white columns; everything else calculates itself.

---

## Why I Built This

As someone active across gym, running, swimming, cycling, and tennis, I wanted a single offline tool that aggregates all activity in one place — without relying on a subscription app. Built entirely in Excel using cross-sheet formulas, MET-based calorie science, and automatic performance tracking.

---

## Workbook Structure — 9 Sheets

| Sheet | What It Does |
|---|---|
| 📊 **Daily Analysis** | Master dashboard — auto-aggregates all 8 activities by date |
| 💪 **Gym** | Strength log — tracks Squat, Bench, Deadlift, OHP, Row with best/latest auto-tracking |
| 🤸 **Workout** | Flexible workout log — yoga, HIIT, mobility with per-row MET entry |
| 🏃 **Run** | Running log — auto-calculates pace, speed, calories |
| 🚶 **Walk** | Walking log — distance, steps, speed, calories |
| 🏊 **Swim** | Swimming log — distance in metres, pace per 100m, calories |
| 🚴 **Cycle** | Cycling log — distance, speed, calories |
| 🎾 **Tennis** | Tennis log — duration, session type, calories |
| 🧖 **Sauna** | Recovery tracker — temperature, type, feel rating |

---

## Key Features

### ✅ Daily Analysis Dashboard
- **Profile section** — enter body weight, target weight, height once → all calorie formulas reference these automatically
- **Overall Totals** — total sessions, active minutes, calories burned, active days, avg min per active day
- **Activity breakdown table** — sessions, total minutes, total calories per sport
- **Daily log** — one row per date showing every activity side by side with active minutes and calories
- Everything auto-populates from the individual sport tabs — no manual summarisation needed

### ✅ MET-Based Calorie Calculation
Uses scientifically validated **MET (Metabolic Equivalent of Task)** values:

| Activity | MET Value |
|---|---|
| Gym / Strength | 5.5 |
| Run | 9.0 |
| Walk | 3.5 |
| Swim | 7.0 |
| Cycle | 6.8 |
| Tennis | 6.5 |
| Workout (flexible) | Per row — yoga ≈ 3, HIIT ≈ 8, mobility ≈ 2.5 |
| Sauna | Not counted — recovery only |

**Formula:** `Calories = MET × Body Weight (kg) × Duration (hours)`

### ✅ Strength Tracking (Gym Sheet)
- Tracks 5 core compound lifts: **Squat, Bench Press, Deadlift, Overhead Press, Row**
- **Best (kg)** — auto-updates to your all-time best for each lift
- **Latest (kg)** — always shows your most recent session weight
- RPE (Rate of Perceived Exertion) column for intensity tracking

### ✅ Performance Records (Auto-Calculated)

| Sheet | Auto-Tracked Records |
|---|---|
| Run | Best pace (min/km), longest run (km), avg speed (km/h) |
| Walk | Longest walk (km), total steps, avg speed |
| Swim | Best pace (min/100m), longest swim (m) |
| Cycle | Longest ride (km), avg speed (km/h) |
| Gym | Best and latest weight per lift |

### ✅ RPE Tracking
Rate of Perceived Exertion logged per session across Gym, Run, Swim, Cycle, and Tennis.

### ✅ Sauna Recovery Log
- Tracked separately — does NOT count toward calorie totals
- Logs: duration, temperature (°C), session type (dry/wet/infrared), feel rating, notes
- Built-in safety note: keep sessions short with high BP, hydrate well, stop if dizzy

### ✅ Flexible Workout Sheet
- Handles any workout not covered by dedicated sheets
- Enter MET per row — yoga ≈ 3, HIIT ≈ 8, mobility ≈ 2.5
- Calories calculate automatically

---

## How To Use — Step by Step

### Step 1 — Set Up Your Profile
1. Open in **Microsoft Excel**
2. Go to **Daily Analysis** sheet
3. Fill in the **PROFILE** section:
   - Body Weight (kg)
   - Target Weight (kg)
   - Height (cm)
4. All calorie formulas now use your weight automatically ✅

### Step 2 — Log a Gym Session
1. Click the **Gym** tab
2. Fill **white columns** only:
   - Date, Focus (Push/Pull/Legs), weights (kg), Duration (min), RPE, Notes
3. Calories calculate automatically
4. Best and Latest rows update automatically

### Step 3 — Log a Run
1. Click the **Run** tab
2. Fill in: Date, Distance (km), Duration (min), RPE, Notes
3. Pace (min/km), Speed (km/h), Calories → all automatic

### Step 4 — Log a Swim
1. Click the **Swim** tab
2. Fill in: Date, Distance **(metres)**, Duration (min), RPE
3. Pace (min/100m) and Calories → automatic

### Step 5 — Log Walk / Cycle / Tennis
Same pattern — fill white columns, coloured columns calculate themselves.

### Step 6 — Log Sauna Recovery
1. Click **Sauna** tab
2. Fill in: Date, Duration, Temp (°C), Type, Feel, Notes
3. Does not add to calorie totals — recovery tracking only

### Step 7 — Check Daily Analysis
1. Return to **Daily Analysis**
2. Everything updates automatically — totals, breakdown, daily log
3. No manual entry needed on this sheet ✅

---

## Colour Rule

| Cell Colour | Meaning | What To Do |
|---|---|---|
| **White** | Input field | ✅ Fill these in |
| **Coloured** | Formula cell | ❌ Do not edit |

---

## Formula Highlights

- `SUMIF` / `SUMIFS` — aggregate calories and minutes per activity into Daily Analysis
- `MAX` / `MIN` — auto-track best pace, heaviest lift, longest session
- `IFERROR` — handles empty rows without showing errors
- `COUNTIF` — counts active sessions and active days
- `AVERAGE` — avg session duration, avg sauna temperature
- Cross-sheet references — Daily Analysis pulls live from all 8 sport tabs

---

## MET Reference Guide (for Workout Sheet)

| Workout Type | MET |
|---|---|
| Yoga | 3.0 |
| Pilates | 3.0 |
| Mobility / Stretching | 2.5 |
| HIIT | 8.0 |
| CrossFit | 7.0 |
| Boxing / Martial Arts | 7.8 |
| Dance | 5.0 |

---

## Repository Structure

```
.
├── Fitness-Tracker_1.xlsx    # Full workbook — all 9 sheets
└── README.md
```

---

## Tools Used

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)

- **Microsoft Excel** — formula-driven cross-sheet workbook
- **Functions:** SUMIF, SUMIFS, MAX, MIN, AVERAGE, COUNTIF, IFERROR, IF
- **Science:** MET-based calorie model (American College of Sports Medicine standard)

---

*Personal project by Sai Krishna Sudarsan | Auckland, New Zealand*
*Active across gym, running, swimming, cycling, and tennis — tracked with Garmin Fenix 8*
