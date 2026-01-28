# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a personal weekly planning and task management system using markdown and git version control. The core file is `weekly-plan.md`, which tracks work projects, personal goals, daily schedules, and progress on various initiatives.

## ⚠️ CRITICAL RULE: Always Verify Current Date

**BEFORE making ANY schedule-related updates, ALWAYS verify the current date and day of week.**

When the user says "ready for morning prep" or asks about "today":

1. **Check the current date** from system environment or ask the user to confirm
2. **Verify the day of week** matches what you expect
3. **Cross-reference with calendar events** - if fetching calendar, ensure the date matches
4. **Never assume** the date based on what's in the plan file - the file may be from a previous session

**Example Check:**
- User says: "Ready for morning prep"
- YOU MUST ASK OR VERIFY: "Just to confirm, today is [day of week], [Month] [Date], correct?"
- OR use system date/time if available
- DO NOT proceed with schedule updates until date is confirmed

This prevents critical errors where the entire day's planning is done for the wrong date.

## Key Workflow

The primary workflow is updating `weekly-plan.md` throughout the week, then committing and pushing changes:

```bash
git add weekly-plan.md
git commit -m "Descriptive message about what was updated"
git push origin main
```

## weekly-plan.md Structure

The file follows a hierarchical structure organized by time scope:

1. **Monthly Sprints** - High-level themes and sprint goals with review dates
2. **Weekly Balance** - Current week's key deliverables and must-dos
3. **Work Projects** (Max 2 active) - Tracked with progress bars, milestones, and sprint targets
4. **Professional Development** - Technical learning goals (e.g., Kotlin coroutines)
5. **Health & Fitness** - Personal health goals with progress tracking
6. **Personal Projects** (Max 2 active) - Home projects, family activities, etc.
7. **Daily Sections** - Each day gets its own section with:
   - Morning review checklist
   - Calendar (work + personal commitments)
   - Available work blocks
   - Today's priorities (CAN'T MISS, Work Focus, Personal MUST DO, If Time Permits)
   - End of day review
8. **Weekly Key Deadlines** - Day-by-day breakdown of the current week

## Progress Tracking Conventions

- **Progress bars**: `████░░░░░░ 40%` format showing visual completion
- **Checkboxes**: `[ ]` for incomplete, `[✓]` for complete, `[→]` for current focus
- **Sprint targets**: Each project has a sprint target percentage to hit by month-end
- **Milestones**: Projects broken into clear milestones with current focus marked

## Daily Planning Pattern

1. **Morning Review** (5 min) - Review calendar, choose workout time, identify top priority
2. **During the Day** - Check off completed items as you go
3. **End of Day Review** (5 min) - Assess completion, plan tomorrow, brain dump any anxieties

## Time Management

- All times are in **Mountain Time (America/Denver)**
- Calendar shows both work commitments and personal commitments
- Available work blocks are calculated between meetings
- Workout time is explicitly chosen each morning (noon, 4:30 PM, or 5:30 PM options)

## Commit Message Patterns

Good commit messages describe what changed in the plan:
- "Tuesday Jan 27 morning prep - complete update"
- "Mark booster strap ordered; Originations Technical Sync cancelled"
- "Add Professional Development section with Kotlin Coroutines mastery goal"
- "Update Big Sky and Presidents Weekend dates"

## Important Notes

- When updating dates/times, verify all related references are updated (sprint goals, milestones, weekly deadlines, etc.)
- The "Max 2 active" rule for projects keeps focus - additional projects go to "Background Projects (Deprioritized)"
- Daily sections accumulate throughout the week - completed days remain visible with their accomplishments
- Personal and work commitments are tracked side-by-side to maintain life balance
