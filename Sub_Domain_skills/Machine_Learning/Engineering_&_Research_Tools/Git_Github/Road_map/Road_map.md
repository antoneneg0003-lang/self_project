# 🧪 Git Command Practice Guide
(Based on full command reference)

This file tells you WHAT to practice for each command family.
Do not memorize. Practice deliberately.

------------------------------------------------------------
0️⃣ GLOBAL OPTIONS
------------------------------------------------------------
Goal:
Understand how Git behaves globally and per-command.

Practice:
- Run git with -C in another directory
- Override config temporarily using -c
- Disable pager using --no-pager
- Use help system to explore unknown commands

Mastery Check:
Can you discover a new Git feature without Google?

------------------------------------------------------------
1️⃣ CONFIG
------------------------------------------------------------
Goal:
Control Git behavior confidently.

Practice:
- Set global name/email
- Change default branch to main
- Enable pull.rebase
- Enable rerere
- View config origin using --show-origin
- Create custom alias (lg = log graph)

Mastery Check:
Can you explain difference between global, local, system config?

------------------------------------------------------------
2️⃣ INIT / CLONE
------------------------------------------------------------
Goal:
Understand repository creation types.

Practice:
- Create normal repo
- Create bare repo
- Clone specific branch
- Clone shallow with --depth=1
- Clone mirror repo

Mastery Check:
When should you use --bare?

------------------------------------------------------------
3️⃣ STATUS / LOG / DIFF
------------------------------------------------------------
Goal:
Inspect repository state precisely.

Practice:
- Compare working vs staged changes
- Use log with --graph --decorate --all
- Filter logs by author/date
- Compare two commits with diff
- Use --name-only and --stat

Mastery Check:
Can you visualize branch topology without GUI?

------------------------------------------------------------
4️⃣ ADD / RM / MV
------------------------------------------------------------
Goal:
Control staging precisely.

Practice:
- Stage all vs only tracked files
- Use git add -p (patch mode)
- Remove file but keep locally (--cached)
- Rename file using git mv
- Test force add of ignored file

Mastery Check:
Can you stage only part of a file?

------------------------------------------------------------
5️⃣ COMMIT
------------------------------------------------------------
Goal:
Create clean history.

Practice:
- Commit with message
- Amend last commit
- Amend without editing message
- Create empty commit
- Change author/date
- Use verbose mode

Mastery Check:
Can you fix a bad commit message without changing content?

------------------------------------------------------------
6️⃣ BRANCH / SWITCH / CHECKOUT
------------------------------------------------------------
Goal:
Move between histories safely.

Practice:
- Create branch
- Delete branch
- Force delete branch
- Switch back using "-"
- Create orphan branch
- Enter detached HEAD

Mastery Check:
Can you explain detached HEAD without confusion?

------------------------------------------------------------
7️⃣ MERGE
------------------------------------------------------------
Goal:
Combine work safely.

Practice:
- Merge with fast-forward
- Merge with --no-ff
- Trigger conflict intentionally
- Abort merge
- Continue after resolving conflict

Mastery Check:
Can you resolve a merge conflict manually?

------------------------------------------------------------
8️⃣ REBASE
------------------------------------------------------------
Goal:
Rewrite history safely.

Practice:
- Rebase feature onto main
- Interactive rebase squash commits
- Use --onto
- Skip commit during rebase
- Abort rebase mid-conflict

Mastery Check:
Can you explain difference between merge vs rebase?

------------------------------------------------------------
9️⃣ RESET / RESTORE / REVERT
------------------------------------------------------------
Goal:
Undo safely and correctly.

Practice:
- reset --soft / --mixed / --hard
- restore staged file
- restore file from old commit
- revert public commit
- revert merge commit

Mastery Check:
When should you NEVER use reset --hard?

------------------------------------------------------------
🔟 STASH
------------------------------------------------------------
Goal:
Pause work cleanly.

Practice:
- Stash tracked only
- Stash including untracked
- Stash with message
- Apply without pop
- Create branch from stash

Mastery Check:
Can you switch branches with unfinished work safely?

------------------------------------------------------------
1️⃣1️⃣ REMOTES
------------------------------------------------------------
Goal:
Work with GitHub properly.

Practice:
- Add remote
- Change remote URL
- Fetch and inspect differences
- Pull with --rebase
- Push with -u
- Push with --force-with-lease
- Delete remote branch

Mastery Check:
Can you fix non-fast-forward error correctly?

------------------------------------------------------------
1️⃣2️⃣ TAGS
------------------------------------------------------------
Goal:
Version control releases.

Practice:
- Create annotated tag
- Delete tag
- Push specific tag
- Verify signed tag (if configured)

Mastery Check:
What’s difference between lightweight and annotated tag?

------------------------------------------------------------
1️⃣3️⃣ CLEAN
------------------------------------------------------------
Goal:
Remove unwanted files safely.

Practice:
- Preview delete with -n
- Remove only ignored files
- Remove everything including ignored

Mastery Check:
Do you always preview before using -f?

------------------------------------------------------------
1️⃣4️⃣ HISTORY ANALYSIS
------------------------------------------------------------
Goal:
Investigate code history deeply.

Practice:
- Use blame for specific lines
- Use bisect to find bug
- Use log -S and -G
- Use shortlog for contributor summary
- Compare two commit ranges

Mastery Check:
Can you find who introduced a bug?

------------------------------------------------------------
1️⃣5️⃣ WORKTREE
------------------------------------------------------------
Goal:
Multiple working directories.

Practice:
- Add new worktree
- Remove worktree
- List worktrees

Mastery Check:
When is worktree better than branch switching?

------------------------------------------------------------
1️⃣6️⃣ SUBMODULE
------------------------------------------------------------
Goal:
Embed repository inside repo.

Practice:
- Add submodule
- Initialize
- Update recursive
- Deinit

Mastery Check:
What problem does submodule solve?

------------------------------------------------------------
1️⃣7️⃣ PATCH WORKFLOW
------------------------------------------------------------
Goal:
Share commits as patches.

Practice:
- Create patch with format-patch
- Apply patch with apply
- Apply mailbox patch with am

Mastery Check:
Difference between apply and am?

------------------------------------------------------------
1️⃣8️⃣ ARCHIVE
------------------------------------------------------------
Goal:
Export project without .git folder.

Practice:
- Create zip archive
- Create tar archive

Mastery Check:
When would you use archive instead of clone?

------------------------------------------------------------
1️⃣9️⃣ STAGING CONTROL / INDEX
------------------------------------------------------------
Goal:
Understand staging internals.

Practice:
- Assume unchanged
- Skip worktree
- Inspect index entries

Mastery Check:
Difference between assume-unchanged vs skip-worktree?

------------------------------------------------------------
2️⃣0️⃣ REF / OBJECT INSPECTION
------------------------------------------------------------
Goal:
Understand Git internals.

Practice:
- Inspect object type with cat-file
- Hash file manually
- View tree structure
- Rev-parse HEAD
- List refs

Mastery Check:
What are commit/tree/blob objects?

------------------------------------------------------------
2️⃣1️⃣ REWRITE HISTORY
------------------------------------------------------------
Goal:
Dangerous rewriting.

Practice:
- filter-branch on test repo
- Use replace
- Rebase preserving merges

Mastery Check:
Why is rewriting public history dangerous?

------------------------------------------------------------
2️⃣2️⃣ MERGE STRATEGIES
------------------------------------------------------------
Goal:
Control conflict resolution behavior.

Practice:
- Merge with -X ours
- Merge with -X theirs
- Try rerere

Mastery Check:
Difference between -s ours vs -X ours?

------------------------------------------------------------
2️⃣3️⃣ HOOKS
------------------------------------------------------------
Goal:
Automate rules.

Practice:
- Create pre-commit hook
- Create pre-push hook

Mastery Check:
Where are hooks stored?

------------------------------------------------------------
2️⃣4️⃣ BUNDLE
------------------------------------------------------------
Goal:
Offline transfer of repo.

Practice:
- Create bundle
- Clone from bundle

Mastery Check:
When is bundle useful?

------------------------------------------------------------
2️⃣5️⃣ SPARSE CHECKOUT
------------------------------------------------------------
Goal:
Checkout only part of repo.

Practice:
- Enable sparse mode
- Set folder restriction

Mastery Check:
Why is sparse useful for large monorepos?

------------------------------------------------------------
2️⃣6️⃣ LFS
------------------------------------------------------------
Goal:
Handle large files.

Practice:
- Track file type
- Push LFS file

Mastery Check:
What problem does LFS solve?

------------------------------------------------------------
2️⃣7️⃣ PERFORMANCE / DEBUG
------------------------------------------------------------
Goal:
Diagnose issues.

Practice:
- Use GIT_TRACE
- Run git maintenance
- Enable fsmonitor

Mastery Check:
How do you debug slow fetch?

------------------------------------------------------------
2️⃣8️⃣ NOTES
------------------------------------------------------------
Goal:
Attach metadata to commits.

Practice:
- Add note
- Push notes
- Remove note

Mastery Check:
When are notes useful?

------------------------------------------------------------
2️⃣9️⃣ DETACHED HEAD
------------------------------------------------------------
Goal:
Avoid losing work.

Practice:
- Enter detached state
- Create branch from detached commit

Mastery Check:
Why does detached HEAD exist?

------------------------------------------------------------
3️⃣0️⃣ CHERRY-PICK
------------------------------------------------------------
Goal:
Move specific commits.

Practice:
- Pick single commit
- Pick range
- Abort conflict

Mastery Check:
When is cherry-pick better than merge?

------------------------------------------------------------
END
