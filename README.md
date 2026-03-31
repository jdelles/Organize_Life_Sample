# Operation Organize Life — Starter Kit

**A personal operating system built with Claude + Google Drive + plain Markdown files.**

This folder contains everything you need to follow along and build your own version of this system. All files use plain text (`.md`) so they work anywhere — no special software required.

---

## What's in this folder

```
sample/
├── README.md                    ← You are here
├── CLAUDE.md                    ← Working memory / briefing doc for Claude
├── TASKS.md                     ← Your central task list
│
├── memory/                      ← Persistent context files (Claude reads these each session)
│   ├── user_profile.md          ← Who you are, your household, your priorities
│   ├── custody_schedule.md      ← (Optional) Kids' schedule & dinner headcount
│   ├── weekly_routine.md        ← Recurring patterns that affect planning
│   ├── food_preferences.md      ← Dietary needs, allergies, likes/dislikes
│   └── fitness_profile.md       ← Exercise habits, equipment, goals
│
├── Recipes/
│   ├── RECIPES_INDEX.md         ← Master index of all recipes (tagged & searchable)
│   ├── RECIPE_TEMPLATE.md       ← Template for adding new recipes
│   └── example-chicken-quesadillas.md  ← A real example to show the format
│
├── Fitness/
│   └── WORKOUT_CONTEXT.md       ← Your fitness context — read by the plan generator
│
├── Maintenance/
│   └── HOME_MAINTENANCE.md      ← Seasonal home maintenance schedule
│
├── Events/
│   └── EVENT_SOURCES.md         ← Curated list of local event sources (customize for your area)
│
└── LinkedIn/
    └── LEARNING_LOG.md          ← Running log that feeds a LinkedIn content generator
```

---

## How to set this up (30 minutes)

### Step 1: Create your Google Drive folder

Create a folder in Google Drive called `Claude` (or whatever you want). This is where everything lives.

Make sure **Google Drive for Desktop** is installed so the folder syncs to your computer as a real folder — this is what lets Claude read and write files directly.

### Step 2: Copy these files into your folder

Drop the entire contents of this `sample/` folder into your `Claude/` folder in Google Drive. You'll customize them in the next step.

### Step 3: Customize the files

Work through each file and fill in the `[PLACEHOLDER]` sections with your own information:

1. **Start with `CLAUDE.md`** — fill in your name, household info, and active projects. This is the first thing Claude reads each session.

2. **Fill in `memory/user_profile.md`** — describe yourself, your partner, your household setup, and your priorities.

3. **Fill in `memory/food_preferences.md`** — this is the most important one if you want meal planning. Be thorough. Include allergies (treated as hard constraints), dislikes, and health goals.

4. **Fill in `memory/fitness_profile.md`** — your current activity, your equipment, your goals.

5. **Fill in `memory/weekly_routine.md`** — what nights are rushed? When do you eat out? What are the recurring patterns in your week?

6. **Update `Fitness/WORKOUT_CONTEXT.md`** — this gets read by Claude when generating workout plans.

7. **Customize `Events/EVENT_SOURCES.md`** — replace the placeholder URLs with real sources for your city.

8. **Skip `memory/custody_schedule.md`** if it doesn't apply to you.

### Step 4: Start a conversation

Open Claude (Claude.ai or the desktop app). Say something like:

> "I've set up a folder in Google Drive at `My Drive/Claude/`. Please read `CLAUDE.md` and the files in the `memory/` folder so you understand our household and can help me plan."

Claude will read the files and from that point forward, it has context about your life. You won't need to re-explain the basics.

---

## Key prompts to get started

Once set up, try these:

**Meal planning:**
> "Generate a meal plan for this week. Read my custody schedule, weekly routine, and food preferences from the memory folder first."

**Workout plan:**
> "Generate this week's workout plan based on `Fitness/WORKOUT_CONTEXT.md`."

**Home maintenance:**
> "What home maintenance tasks are due this month based on `Maintenance/HOME_MAINTENANCE.md`?"

**Add a recipe:**
> "Add a new weeknight salmon recipe to my recipe library. Use the template in `Recipes/RECIPE_TEMPLATE.md` and update `Recipes/RECIPES_INDEX.md`."

**Task management:**
> "Check my `TASKS.md` and tell me what's on my plate today."

**Monthly events:**
> "Search the sources in `Events/EVENT_SOURCES.md` and give me a report of things worth doing this month."

---

## The core idea

Everything is designed around one principle: **the knowledge lives in your files, not in the AI.**

Claude is smart but stateless — it doesn't remember last week's conversation. By keeping your context in plain text files that Claude reads at the start of each session, you get the benefit of persistent memory without depending on any particular app or service.

The files are yours. They live in Google Drive. They'll be readable in 20 years. If you switch AI tools, the data comes with you.

---

## What this costs

This system was built using **Claude Pro — approximately $20/month ($200/year on the annual plan)**. No Max tier. No enterprise setup. Just a regular consumer subscription.

The Cowork desktop app (currently in beta) is what enables Claude to read and write files directly on your computer. Without it, you'd copy-paste file contents manually — still workable, just less seamless.

---

## Tips from someone who built this

- **Start with one domain.** Don't try to fill in every file at once. Pick the one that costs you the most time and stress (for most people: meal planning or task management) and get that working first.

- **The recipe library is where the compounding happens.** The more recipes you have in your library, the smarter the meal plans get. Seed it early — add 5-10 recipes in your first session.

- **Update the memory files as life changes.** If a kid's schedule changes, update `custody_schedule.md`. If someone gets injured, update `fitness_profile.md`. The system is only as accurate as the files.

- **Add an automation backlog to `TASKS.md`.** Keep a running list of things you want Claude to automate. Review it monthly and knock one off.

- **The `CLAUDE.md` file is your most important file.** It's the first thing Claude reads. Keep it current and honest — it sets the tone for every session.

---

*Built with Claude Cowork — March 2026*
