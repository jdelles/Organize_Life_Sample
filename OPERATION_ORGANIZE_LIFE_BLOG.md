# Operation Organize Life: How I Used AI to Build a Personal Operating System
*A retrospective on our first weeks — what we built, why it works, and where we're headed*

---

We're a busy household. I'm a software engineer, my wife is a clinical pharmacist, and between us we have four kids — two boys (ages 9 and 11) and two daughters (ages 14 and 17) from previous marriages — with custody schedules that make our family calendar look like a logic puzzle. We're in midlife. We used to be in better shape. Life is full, fast, and frequently chaotic.

A few weeks ago, I decided I was done just reacting to all of it. I wanted a system. Not another app. Not a subscription. A *real* system that learns how we actually live — one I could shape, update, and own. That's how "Operation Organize Life" was born.

Oh — and before I forget to mention it: I'm doing all of this on the **Claude Pro plan, which runs about $20/month ($200 for the year on the annual plan)**. Not the Max tier. Not an enterprise setup. Just a regular consumer subscription, the same one available to anyone. The results have been significant enough that I think the ROI case basically makes itself, but I'll let you draw your own conclusions.

Here's what we've built, how it works, and why I think this approach is genuinely worth writing about.

---

## The Philosophy: Plain Text + AI + Google Drive

Before I get into the specifics, I want to explain the guiding principle, because it shapes every decision we made.

The system is built entirely on plain text Markdown files stored in Google Drive. No special apps. No locked-in SaaS tools. No proprietary databases. Just `.md` files in a folder that syncs automatically to every device I own.

Why does this matter? Portability. If I want to read my meal plan on my phone, I open Google Drive. If I want Claude to read my fitness context and generate a workout plan, it reads the same file. If I switch to a different AI assistant in two years, the data is still there. If Google Drive goes away, I copy the folder somewhere else in five minutes.

Plain text is the most durable, portable, flexible format humans have ever invented. Every other part of the system is built around that bedrock.

The AI layer — Claude — acts as the intelligence on top of these files. It reads them, updates them, and reasons about them. But the *knowledge* lives in the files, not in the AI's memory. That's a crucial distinction.

---

## What We Built

### 1. A Persistent Memory Layer

The first thing we built was a memory system so Claude doesn't walk into every conversation cold. Over our sessions, we captured:

- **Family profile**: who we are, how the household runs, what tools we use
- **Custody schedule**: a precise map of which kids are home on which nights, and the dinner headcount formula that flows from it (dinner is for 2, 4, or 6 people depending on the night and the week)
- **Weekly routine patterns**: two nights a week are drop-off nights — rushed, with no time to cook. Some Tuesdays are Trivia nights where we eat out. Weekends with the boys mean one breakfast out and one dinner out.
- **Fitness profile**: I play basketball three mornings a week; my wife runs two mornings a week. Strength training goes on the other days.
- **Food preferences**: family-specific dislikes, health goals (high fiber, two servings of veg, easy on red meat), and critically — a hard allergy flag for one of the kids that Claude checks against every recipe, automatically.

These aren't just notes. They're structured files that Claude reads at the start of each session. When I ask for a meal plan, it already knows how many people are eating that night, which nights are rushed, and which recipes need to be allergy-checked. I don't explain any of that. It just works.

**Time saved**: Easily 10–15 minutes per planning conversation, eliminated entirely.

---

### 2. A Recipe Library

We built a recipe library from scratch — 15 recipes so far, each in its own Markdown file. Every recipe is tagged: weeknight-ok, meal-prep, kid-friendly, gluten-free, omega-3, and so on. There's a master `RECIPES_INDEX.md` that serves as a lookup table.

This might sound like a lot of work upfront, but the payoff is immediate. When Claude generates a weekly meal plan, it's pulling from *our* actual recipe library — not a random internet suggestion. It knows which recipes store well for batch cooking, which ones are quick enough for a rushed weeknight, and which ones the kids will actually eat.

The recipes themselves are simple: ingredients scaled to servings, instructions, tags, rough nutrition notes. Nothing fancy. But having them in a consistent format means the AI can reason about them systematically.

We also built a sample weekly meal plan and a live plan for the current week, complete with a Sunday prep guide — what to batch cook, what to pre-chop, what to set aside for the rushed nights.

**Time saved**: Meal planning used to take 30–45 minutes a week of "what are we making, what do we have, who's home." Now it's a 5-minute conversation.

---

### 3. A Fitness System

We built a `WORKOUT_CONTEXT.md` file that describes our equipment (kettlebells, a rowing machine, jump rope, yoga mat), our current activity levels, and our goals. Claude reads this and generates weekly workout plans that actually fit our lives — not generic fitness content.

The workout plan accounts for the fact that I already get significant cardio from basketball three days a week, so strength training on those days would be counterproductive. It accounts for the fact that we're prioritizing muscle maintenance and cognitive health over performance metrics. It accounts for our schedule.

We also documented the philosophy: workouts should be 30–45 minutes max, sustainable, and home-based. No gym required.

As we add equipment or our situation changes, we update the context file, and every future plan automatically reflects the new reality.

**Time saved**: No more searching YouTube for workout routines or wondering if we're missing something important for our health goals.

---

### 4. A Home Maintenance System

We built a seasonal home maintenance schedule tailored to our specific area — not a generic list, but one that accounts for the local climate, our specific home, and our two vehicles.

It's broken into weekly, monthly, seasonal, and annual tasks. There's a separate monthly reminder file that extracts just what's due right now. The whole thing is designed so that at the start of each month, Claude can read the master schedule and output exactly what needs attention — no more scrambling to remember that the HVAC filter needs changing or that the lawn fertilizer window is closing.

**Time saved**: Roughly one "oh no, we forgot to do X" crisis averted per month.

---

### 5. A Local Events System

We wanted to be more intentional about our social life and family experiences. So we built a curated list of event sources for our area — local calendars, family activity sites, farmers markets, seasonal festivals, live music venues.

Each month, Claude can pull from these sources and generate a report of things worth doing. The sources are tagged with why they're useful and when they're relevant. Family interests are documented: outdoor events, festivals, farmers markets, kid-friendly activities across a range of ages, live music.

The vision is a monthly "here's what's worth doing this month" digest that replaces the endless scrolling and last-minute scrambling we do now.

---

### 6. A LinkedIn / Professional Growth Log

I want to stay active on LinkedIn but I'm not interested in producing content for its own sake. So we built a `LEARNING_LOG.md` — a running journal where I drop notes on things I'm learning or building in AI/ML. The content generator reads from this log and surfaces post ideas grounded in what I'm *actually* experiencing, not manufactured hot takes.

The constraint is intentional: Claude won't generate fluff. It only works with real entries. If the log is empty, there's nothing to write about, which is the right forcing function.

---

### 7. A Working Memory File (CLAUDE.md)

One of the most important pieces is a file called `CLAUDE.md` in the root of the Google Drive Claude folder. This is a briefing document — it tells Claude who we are, what the active projects are, what tools are connected, and what rules to follow in every session.

It's essentially the "pre-meeting brief" that Claude reads before we start working. It means I never have to re-explain the basics. The file is updated as our situation changes.

---

### 8. A Task Management System

We have a `TASKS.md` in Google Drive that serves as the central task list. It's organized by time horizon: today, this week, next week, someday, and a dedicated "automation backlog" section for Claude-specific workflows we want to build.

It's not a sophisticated project management tool. It's a text file. And it's exactly right for our needs.

---

## Why This Approach Works

**It's cumulative.** Every conversation adds to the system. Every preference we establish, every constraint we document, every recipe we add — it compounds. The system gets smarter about our life over time without requiring us to maintain some elaborate database.

**It's honest.** The files reflect reality. If I want Claude to help me with meal planning, it's working from how our family actually eats, not an idealized version. The custody schedule in the memory file is the real custody schedule, not a simplified approximation.

**It's low-friction.** I don't have to open an app, navigate a dashboard, or maintain a complex workflow. I open a conversation, describe what I need, and the system already has most of the context it needs. For recurring tasks, we're building scheduled automations that run without me prompting at all.

**It's affordable.** This is all running on the Claude Pro plan — roughly $20/month, or around $200 annually. Not a specialized enterprise tool. Not a custom integration. A consumer subscription and some well-organized text files.

**It's portable and durable.** All the knowledge lives in Google Drive as plain Markdown files. If I want to open them in a text editor, I can. If I want to share them with my wife, I can. If I want to version-control them with git, I can. The format will still be readable in 20 years.

---

## What We'd Do Differently

**Start the recipe library earlier.** The recipe library is where we get the most leverage. If I'd started adding recipes from week one instead of week two, we'd have a deeper rotation by now. If you're building something like this, seed your recipe library first.

**Be more systematic about capturing weekly routine variations.** We have the big patterns documented, but there are edge cases — holiday weeks, school breaks, sports seasons — that would be worth encoding more explicitly. We're building this as we go, but a more thorough upfront capture would reduce the number of corrections needed later.

**Calendar integration sooner.** Right now, the custody schedule lives in memory files. Ideally, it cross-references with our actual calendars. That integration is on the backlog and would make the whole system significantly more powerful.

---

## What We're Building Next

The automation backlog has four big items:

**Finances & Budget Tracking.** Upload monthly bank and credit card statements, have Claude categorize spending and flag patterns, and track a major home renovation budget separately. We want visibility into our money without building a spreadsheet empire.

**Calendar Sync & Conflict Detection.** Get all our calendars fully in sync. Build a scheduled check that flags conflicts and suggests open weekends for events or planning.

**Events × Calendar Cross-Reference.** The monthly events report is useful, but it becomes *much* more useful when cross-referenced against our actual calendar — so it can say "you have a free Saturday the 18th and there's a festival nearby, here's the drive time."

**LinkedIn Content Generator.** Once the Learning Log has enough entries, build a monthly workflow that reads the log and surfaces 2–4 grounded post ideas. No fluff, no AI-generated hot takes — just prompts rooted in what I've actually been thinking about and building.

---

## Want to Try This Yourself?

I've put together a folder of sample files that mirror exactly what we built — with placeholder names and prompts so you can adapt them to your own life. You can find them alongside this post.

The setup takes about 30 minutes: create a folder in Google Drive, drop in the files, customize the `CLAUDE.md` and memory files with your own details, and start a conversation. Claude in Cowork mode will pick up the context from there.

The key insight I'd leave you with: don't try to build everything at once. Start with the one domain that costs you the most time and stress. For us it was meal planning. For you it might be home maintenance, or your fitness routine, or task management. Get that one system working well, then add the next one.

The compounding effect kicks in faster than you'd expect.

---

*Written March 30, 2026*
