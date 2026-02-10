# 🎯 Git Mastery Strategy

This file defines HOW to learn and HOW to practice Git.
Commands alone are not mastery.
Application creates mastery.

============================================================

# 📘 1️⃣ Learning Strategy

Core Principle:
Learn → Immediately Apply → Reflect → Repeat

--------------------------------------------

## Rule 1: Immediate Application

After learning a command,
start a small project or scenario that REQUIRES that command.

Example:
- Learn `git branch` → Create feature branch workflow
- Learn `git rebase` → Simulate messy commit cleanup
- Learn `git stash` → Switch tasks mid-work

Never learn passively.
Every command must be tied to action.

--------------------------------------------

## Rule 2: Micro Projects per Concept

For every command family:
- Create a mini-repo
- Simulate real workflow
- Intentionally create mistakes
- Recover using Git tools

Example:
- Create merge conflict intentionally
- Break history using reset
- Recover using reflog

--------------------------------------------

## Rule 3: Build Mental Models

Don’t memorize commands.
Understand structure:

Working Directory
↓
Staging Area (Index)
↓
Commit History (Repository)
↓
Remote

Every command affects one of these layers.
Ask:
"Which layer am I modifying?"

--------------------------------------------

## Rule 4: Learn Through Failure

Intentionally:
- Cause conflicts
- Delete commits
- Push wrong branch
- Detach HEAD

Then recover.

Controlled mistakes build confidence.

--------------------------------------------

## Rule 5: Periodic Review

Weekly:
- Review log graph
- Explain rebase vs merge in your own words
- Rebuild a repo from scratch

If you cannot explain it clearly,
you don’t fully understand it.

============================================================
