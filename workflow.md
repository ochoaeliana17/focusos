# FocusOS — Automation Workflow

How Zapier connects Notion, Claude AI, and the user's daily routine.

---

## Overview
[Time trigger] → [Zapier] → [Claude AI] → [Notion update]
[Notion change] → [Zapier] → [Claude AI] → [Notion update]
---

## Workflow 1 — Morning Daily Plan (8:00 AM daily)

**Trigger:** Zapier schedule — every day at 8:00 AM

**Zapier reads from Notion:**
- All tasks with Status = "To Do" or "In Progress"
- Top priority project this week
- User's energy level (set the night before)

**Zapier sends to Claude:**
- Prompt 1 with task list + project + energy level filled in

**Claude returns:**
- Focused daily plan with top 3 tasks + deep work block

**Zapier writes back to Notion:**
- Daily Plan page updated with Claude's output
- Status updated to "Planned"

---

## Workflow 2 — Task Prioritization (on new task)

**Trigger:** New task added to Notion database

**Zapier reads:**
- Task name, description, deadline, project

**Zapier sends to Claude:**
- Prompt 2 with task details

**Claude returns:**
- Priority score (1-10) + reasoning

**Zapier writes back to Notion:**
- Priority field updated automatically
- No manual scoring needed

---

## Workflow 3 — Evening Habit Check-in (9:00 PM daily)

**Trigger:** Zapier schedule — every day at 9:00 PM

**Zapier reads from Notion:**
- Habits completed today
- Habits missed today
- Current streak
- Points earned today

**Zapier sends to Claude:**
- Prompt 4 with habit data

**Claude returns:**
- Brief honest check-in message

**Zapier writes back to Notion:**
- Evening check-in field updated
- Streak counter updated

---

## Workflow 4 — Weekly Review (Sunday 6:00 PM)

**Trigger:** Zapier schedule — every Sunday at 6:00 PM

**Zapier reads from Notion:**
- All tasks completed this week
- All tasks not completed
- Habits data for the week
- Points earned
- Current level

**Zapier sends to Claude:**
- Prompt 3 with full week data

**Claude returns:**
- Weekly review with observations, patterns, recommendations

**Zapier writes back to Notion:**
- Weekly Review page created automatically
- Ready to read Monday morning

---

## Stack

| Tool | Role | Cost |
|------|------|------|
| Notion | Database + dashboard + gamification | Free |
| Zapier | Automation layer | Free tier |
| Claude AI | Intelligence layer | API usage |
| GitHub | Documentation | Free |

---

## Time saved

| Task | Manual | With FocusOS |
|------|--------|-------------|
| Morning planning | 20-30 min | 2 min review |
| Task prioritization | 10 min per task | Automatic |
| Habit tracking | 5 min daily | Automatic |
| Weekly review | 45-60 min | Auto-generated |
| **Total** | **2+ hrs/week** | **under 10 min** |