# FocusOS — Gamification System

The points, levels, and streaks system built entirely inside Notion.

---

## Points System

| Action | Points |
|--------|--------|
| Complete a task (Low priority) | +5 pts |
| Complete a task (Medium priority) | +10 pts |
| Complete a task (High priority) | +20 pts |
| Complete a task early (before deadline) | +5 bonus pts |
| Complete daily habit | +5 pts per habit |
| Perfect habit day (all habits done) | +15 bonus pts |
| 7-day streak | +50 bonus pts |
| 30-day streak | +200 bonus pts |
| Complete a full project | +100 pts |

---

## Level System

| Level | Name | Points Required | Reward |
|-------|------|----------------|--------|
| 1 | Starter | 0 pts | — |
| 2 | Builder | 100 pts | Unlock Weekly Review |
| 3 | Focused | 300 pts | Unlock AI Daily Plan |
| 4 | Momentum | 600 pts | Unlock Project Analytics |
| 5 | Flow State | 1,000 pts | Unlock Full FocusOS |
| 6 | Optimizer | 2,000 pts | Custom AI prompts |
| 7 | Master | 5,000 pts | — |

---

## Streaks

A streak is the number of consecutive days where the user:
- Completed at least 1 High priority task
- Tracked at least 1 habit

Streaks reset to 0 if either condition is missed.

---

## Notion Formula — Points Calculation

For each task row in Notion, the points are calculated automatically:
if(prop("Status") == "Done",
if(prop("Priority") == "High", 20,
if(prop("Priority") == "Medium", 10, 5))

if(prop("Completed Date") <= prop("Deadline"), 5, 0),
0.


---

## Notion Formula — Level Calculation

In the user profile page:
if(prop("Total Points") >= 5000, "7 — Master",
if(prop("Total Points") >= 2000, "6 — Optimizer",
if(prop("Total Points") >= 1000, "5 — Flow State",
if(prop("Total Points") >= 600, "4 — Momentum",
if(prop("Total Points") >= 300, "3 — Focused",
if(prop("Total Points") >= 100, "2 — Builder",
"1 — Starter"))))))
---

## Dashboard view in Notion

The FocusOS dashboard shows:
- Current level + points to next level
- Today's AI-generated plan
- Active streak counter
- Top 3 tasks for today
- Habit completion rings
- Weekly points chart