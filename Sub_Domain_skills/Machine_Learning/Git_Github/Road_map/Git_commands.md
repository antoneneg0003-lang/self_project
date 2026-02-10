# ============================================
# 🔥 GIT MASTER COMMAND + GLOBAL FLAG REFERENCE
# ============================================

# ============================================
# 0️⃣ GLOBAL GIT OPTIONS (work with ANY command)
# ============================================

git --version
  # Show installed Git version

git --help
git help <command>
  # Open manual page

git -C <path> <command>
  # Run Git command as if inside another directory

git -c <key>=<value> <command>
  # Temporarily override config for one command

git --exec-path
  # Show Git internal command path

git --html-path
  # Show documentation location

git --man-path
  # Show man page path

git --config-env=<name>=<envvar>
  # Read config value from environment variable

git --no-pager <command>
  # Disable pager (less)

git --paginate <command>
  # Force pager

# ============================================
# 1️⃣ CONFIGURATION
# ============================================

git config
  --global        # user-level config (~/.gitconfig)
  --system        # system-wide config (/etc/gitconfig)
  --local         # repo-specific (.git/config)
  --list          # list all configs
  --show-origin   # show where each config came from
  --get <key>
  --set <key> <value>
  --unset <key>
  --edit
  --remove-section <section>

# ============================================
# 2️⃣ INIT / CLONE
# ============================================

git init
  --bare                  # create bare repository
  --initial-branch=<name>
  --template=<dir>

git clone <url>
  -b, --branch <name>     # checkout specific branch
  --depth <n>             # shallow clone
  --single-branch
  --recurse-submodules
  --mirror
  --origin <name>

# ============================================
# 3️⃣ STATUS / INSPECTION
# ============================================

git status
  -s, --short
  -b, --branch
  --ignored
  --untracked-files=all

git log
  --oneline
  --graph
  --decorate
  --all
  -p                     # patch view
  --stat
  --author=<name>
  --since=<date>
  --until=<date>
  -n <number>

git show <commit>
  --stat
  --name-only

git diff
  --staged
  --cached
  --stat
  --name-only

# ============================================
# 4️⃣ ADD / REMOVE / MOVE
# ============================================

git add
  -A, --all
  -u, --update
  -p, --patch
  -f, --force
  -n, --dry-run

git rm
  -f, --force
  -r, --recursive
  --cached

git mv
  -f

# ============================================
# 5️⃣ COMMIT
# ============================================

git commit
  -m, --message <msg>
  -a, --all
  --amend
  --no-edit
  --author=<name>
  --date=<date>
  --allow-empty
  -v, --verbose
  --signoff

# ============================================
# 6️⃣ BRANCH / SWITCH / CHECKOUT
# ============================================

git branch
  -a
  -r
  -v
  -vv
  -d
  -D
  -m
  -M
  --list

git switch
  -c                 # create and switch
  -C                 # force create
  --detach

git checkout
  -b
  -B
  --detach
  --orphan

# ============================================
# 7️⃣ MERGE / REBASE
# ============================================

git merge
  --no-ff
  --ff-only
  --squash
  --abort
  --continue

git rebase
  -i, --interactive
  --abort
  --continue
  --skip
  --rebase-merges
  --onto <newbase>

# ============================================
# 8️⃣ RESET / RESTORE / REVERT
# ============================================

git reset
  --soft
  --mixed
  --hard
  --merge
  --keep

git restore
  --staged
  --source=<commit>

git revert
  --no-commit
  --edit

# ============================================
# 9️⃣ STASH
# ============================================

git stash
  push
    -m <msg>
    -u, --include-untracked
    -a, --all
  list
  show
  pop
  apply
  drop
  clear

# ============================================
# 🔟 REMOTES
# ============================================

git remote
  add
  remove
  rename
  -v
  show

git fetch
  --all
  --prune
  --tags

git pull
  --rebase
  --no-rebase
  --ff-only

git push
  -u, --set-upstream
  -f, --force
  --force-with-lease
  --tags
  --delete

# ============================================
# 1️⃣1️⃣ TAGS
# ============================================

git tag
  -a
  -d
  -l
  -m <msg>
  --annotate

# ============================================
# 1️⃣2️⃣ CLEAN
# ============================================

git clean
  -f
  -d
  -x
  -X
  -n

# ============================================
# 1️⃣3️⃣ INTERNAL / ADVANCED
# ============================================

git reflog
git fsck
git gc
git cat-file -p <hash>
git rev-parse HEAD
git count-objects -vH
git ls-files
git ls-tree
git hash-object
git update-index

# ============================================
# 1️⃣4️⃣ HISTORY ANALYSIS / SEARCH
# ============================================

git blame <file>
  -L <start>,<end>        # specific lines
  --show-email

git bisect
  start
  bad <commit>
  good <commit>
  run <script>
  reset

git shortlog
  -s                      # summary
  -n                      # numeric sort
  -e                      # show email

git describe
  --tags
  --all

git cherry <upstream> <branch>

git range-diff <old> <new>

git log --grep=<pattern>
git log -S<string>         # search changes by string
git log -G<regex>          # search by regex diff


# ============================================
# 1️⃣5️⃣ WORKTREES (Multiple working dirs)
# ============================================

git worktree add <path> <branch>
git worktree list
git worktree remove <path>
git worktree prune


# ============================================
# 1️⃣6️⃣ SUBMODULES
# ============================================

git submodule add <repo>
git submodule init
git submodule update
  --recursive
  --remote

git submodule status
git submodule deinit


# ============================================
# 1️⃣7️⃣ PATCH / APPLY
# ============================================

git apply <patch>
  --check
  --reject

git am <patch>
  --continue
  --abort

git format-patch <commit>
  -n <count>
  --stdout


# ============================================
# 1️⃣8️⃣ ARCHIVE / EXPORT
# ============================================

git archive
  --format=zip
  --format=tar
  -o <file>


# ============================================
# 1️⃣9️⃣ STAGING AREA CONTROL
# ============================================

git add -i                 # interactive mode
git update-index
  --assume-unchanged <file>
  --no-assume-unchanged
  --skip-worktree

git check-ignore -v <file>


# ============================================
# 2️⃣0️⃣ REFERENCE / OBJECT INSPECTION
# ============================================

git show-ref
git for-each-ref
git symbolic-ref HEAD
git rev-list <branch>
git rev-parse --abbrev-ref HEAD


# ============================================
# 2️⃣1️⃣ REWRITE HISTORY (DANGEROUS)
# ============================================

git filter-branch
git filter-repo           # external tool (recommended modern)
git rebase -r             # preserve merges
git replace


# ============================================
# 2️⃣2️⃣ MERGE STRATEGIES
# ============================================

git merge -s ours
git merge -s theirs
git merge -X ours
git merge -X theirs
git merge --strategy-option=<option>


# ============================================
# 2️⃣3️⃣ HOOKS
# ============================================

.git/hooks/
  pre-commit
  pre-push
  commit-msg
  post-merge
  post-checkout


# ============================================
# 2️⃣4️⃣ BUNDLE (Offline transfer)
# ============================================

git bundle create repo.bundle --all
git clone repo.bundle
git fetch repo.bundle <branch>


# ============================================
# 2️⃣5️⃣ SPARSE CHECKOUT
# ============================================

git sparse-checkout init
git sparse-checkout set <path>
git sparse-checkout list


# ============================================
# 2️⃣6️⃣ CREDENTIAL MANAGEMENT
# ============================================

git credential-cache
git credential-store
git credential-manager-core


# ============================================
# 2️⃣7️⃣ LARGE FILE SUPPORT
# ============================================

git lfs install
git lfs track
git lfs pull


# ============================================
# 2️⃣8️⃣ PERFORMANCE / DEBUG
# ============================================

GIT_TRACE=1 git <command>
GIT_CURL_VERBOSE=1 git <command>
git config core.fsmonitor
git maintenance run
git maintenance start


# ============================================
# 2️⃣9️⃣ ALIASES (Power productivity)
# ============================================

git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.st status
git config --global alias.lg "log --oneline --graph --all"


# ============================================
# 3️⃣0️⃣ DETACHED HEAD SAFETY
# ============================================

git switch --detach <commit>
git branch <name>         # save detached work


# ============================================
# 3️⃣1️⃣ CHERRY PICK
# ============================================

git cherry-pick <commit>
  -n
  --continue
  --abort
  --skip


# ============================================
# 3️⃣2️⃣ NOTES (Attach metadata to commits)
# ============================================

git notes add -m "note"
git notes show
git notes remove


# ============================================
# 3️⃣3️⃣ ATTRIBUTES
# ============================================

.gitattributes
  text=auto
  merge=ours
  diff=<driver>


# ============================================
# 3️⃣4️⃣ IGNORE DEBUG
# ============================================

git check-ignore -v <file>
git ls-files --others --ignored --exclude-standard


# ============================================
# 3️⃣5️⃣ SAFETY / RECOVERY
# ============================================

git reflog expire
git fsck --lost-found
git restore --source=HEAD~1 <file>



# ============================================================
# 🔥 GIT EXTENDED / POWER-USER / PLUMBING COMMANDS (MORE)
# ============================================================

# ============================================================
# A) HELP / DISCOVERY (find commands you didn’t know exist)
# ============================================================

git help -a                 # list all available Git commands
git help -g                 # list Git concept guides (revisions, config, hooks, etc)
git help revisions          # revision syntax (HEAD^, HEAD~3, A..B, A...B)
git help refspec            # push/fetch refspec rules
git help glossary           # official terms

git <cmd> -h                # quick help for a command
man git-<cmd>               # open man page directly


# ============================================================
# B) REVISION / RANGE SPEC (INSANELY USEFUL)
# ============================================================

# Single commits / ancestors
git show HEAD
git show HEAD^              # parent of HEAD
git show HEAD~3             # 3rd ancestor
git show <hash>^2           # 2nd parent (merge commits)

# Ranges
git log A..B                # commits in B not in A
git log A...B               # symmetric difference
git diff A..B               # diff between tips
git merge-base A B          # common ancestor commit

# Path-limited history
git log -- <path>
git log <rev> -- <path>

# Pick by date-ish selectors (needs reflog sometimes)
git rev-parse @{yesterday}
git rev-parse @{1.week.ago}


# ============================================================
# C) LOG / SHOW FORMATTING (for real analysis)
# ============================================================

git log --pretty=oneline
git log --pretty=short
git log --pretty=full
git log --pretty=fuller
git log --pretty=format:"%h %ad %an %s" --date=short

git log --since="2026-01-01" --until="2026-02-01"
git log --first-parent               # follow mainline
git log --no-merges
git log --merges
git log --reverse
git log --boundary

git show --pretty=fuller <commit>
git show --word-diff
git show --color-moved               # highlights moved code (when supported)

# Compare authors / stats
git log --numstat
git log --shortstat
git log --dirstat
git log --stat-width=120

# Branch topology views
git log --graph --decorate --all --simplify-by-decoration
git show-branch
git name-rev --name-only <hash>


# ============================================================
# D) DIFF ADVANCED (precision diffs)
# ============================================================

git diff --word-diff
git diff --word-diff-regex="[^[:space:]]+"
git diff --color-words
git diff --patience
git diff --histogram
git diff --minimal

git diff -w                           # ignore whitespace
git diff --ignore-space-at-eol
git diff --ignore-cr-at-eol
git diff --ignore-all-space
git diff --ignore-blank-lines

git diff --submodule
git diff --recurse-submodules

git diff <commit>^!                   # diff of a single commit
git diff A...B                        # diff from merge-base

git diff --name-status
git diff --diff-filter=ACMRTUXB       # filter change types


# ============================================================
# E) FILE / CONTENT SEARCH (superpowers)
# ============================================================

git grep "pattern"
git grep -n "pattern"
git grep -p "pattern"                 # show function context (where supported)
git grep --line-number --heading

git log -S "literal_string"           # pick commits where string count changes
git log -G "regex_pattern"            # pick commits where regex diff matches

git blame -w <file>                   # blame ignoring whitespace
git blame --since="2026-01-01" <file>


# ============================================================
# F) REMOTES / NETWORK (advanced)
# ============================================================

git remote -v
git remote show <name>
git remote set-url <name> <newurl>
git remote set-url --add <name> <url>
git remote set-url --delete <name> <url>
git remote prune <name>

git fetch <remote> <refspec>
git fetch --prune --prune-tags
git fetch --recurse-submodules
git fetch --depth=1
git fetch --shallow-since="2026-01-01"
git fetch --unshallow

git pull --rebase --autostash
git pull --recurse-submodules

git push --force-with-lease
git push --atomic
git push --follow-tags
git push --signed                     # push signed tags (depends setup)

git ls-remote --heads <url>
git ls-remote --tags <url>


# ============================================================
# G) STASH ADVANCED
# ============================================================

git stash push -m "msg" --keep-index
git stash push -p                     # interactively select hunks
git stash show -p stash@{0}
git stash branch <newbranch> stash@{0}
git stash apply --index stash@{0}


# ============================================================
# H) TAGS (power)
# ============================================================

git tag -a v1.0 -m "release"
git tag -s v1.0 -m "signed release"   # GPG signed (if configured)
git tag -v v1.0                       # verify signed tag
git push --tags
git push <remote> v1.0


# ============================================================
# I) CONFLICT / MERGE HELPERS
# ============================================================

git mergetool
git mergetool --tool-help

git rerere status                     # reuse recorded conflict resolutions
git rerere diff
git rerere clear


# ============================================================
# J) REBASE / INTERACTIVE POWER
# ============================================================

git rebase -i --rebase-merges
git rebase -i --autosquash            # works with fixup!/squash! commits
git commit --fixup=<commit>
git commit --squash=<commit>

git rebase --onto <newbase> <oldbase> <branch>
git rebase --update-refs              # newer Git versions (keeps refs synced)


# ============================================================
# K) RESET/RESTORE SAFETY RECIPES
# ============================================================

git restore <file>
git restore --staged <file>
git restore --source=<commit> -- <file>

git reset --soft HEAD~1               # undo commit, keep staged
git reset --mixed HEAD~1              # undo commit, keep working
git reset --hard HEAD~1               # destructive

git revert <commit>                   # safe undo by new commit
git revert -m 1 <merge_commit>        # revert a merge (choose mainline parent)


# ============================================================
# L) CHERRY-PICK POWER
# ============================================================

git cherry-pick -x <commit>           # record original hash in message
git cherry-pick -n <commit>           # no commit (stage only)
git cherry-pick A..B                  # pick a range (non-inclusive of A)


# ============================================================
# M) CLEAN (dangerous)
# ============================================================

git clean -nfd                        # preview delete
git clean -xfd                        # remove ignored too (VERY destructive)
git clean -fX                         # remove only ignored


# ============================================================
# N) REFS / BRANCH POINTERS (advanced)
# ============================================================

git branch --contains <commit>
git branch --no-contains <commit>
git branch --merged
git branch --no-merged

git switch -                           # go back to previous branch
git checkout -                         # old equivalent

git update-ref refs/heads/<b> <hash>   # low-level move ref (dangerous)
git symbolic-ref HEAD refs/heads/main  # repoint HEAD (rare)


# ============================================================
# O) NOTES (metadata attached to commits)
# ============================================================

git notes add -m "note text" <commit>
git notes append -m "more"
git notes show <commit>
git notes list
git notes remove <commit>
git push origin refs/notes/*


# ============================================================
# P) REPOSITORY HEALTH / MAINTENANCE
# ============================================================

git fsck --full
git fsck --lost-found
git gc --aggressive
git gc --prune=now
git repack -ad
git prune
git count-objects -vH

git maintenance run
git maintenance start
git maintenance stop


# ============================================================
# Q) PACK / OBJECT DATABASE (PLUMBING)
# ============================================================

git cat-file -t <hash>                # type: commit/tree/blob/tag
git cat-file -p <hash>                # pretty-print object
git cat-file --batch                  # batch queries

git hash-object <file>
git hash-object -w <file>             # write object into db
git mktree
git ls-tree <treeish>
git read-tree <treeish>
git write-tree
git commit-tree <tree_hash> -p <parent_hash> -m "msg"

git rev-list --objects --all
git verify-pack -v .git/objects/pack/*.idx
git index-pack .git/objects/pack/*.pack
git pack-objects --all packtmp


# ============================================================
# R) INDEX / STAGING INTERNALS (PLUMBING)
# ============================================================

git ls-files
git ls-files -s                       # show stage info
git ls-files -u                       # unmerged entries
git update-index --add --cacheinfo <mode> <hash> <path>
git update-index --refresh            # rescan working tree
git update-index --really-refresh


# ============================================================
# S) REFLOG / RECOVERY (must-know)
# ============================================================

git reflog
git reflog show HEAD
git reflog expire --expire=now --all  # dangerous if you still need recovery

# Recover a lost commit (example)
# 1) find hash in reflog, then:
git checkout -b recovered <hash>


# ============================================================
# T) PARTIAL CLONE / PROMISOR (advanced network optimization)
# ============================================================

git clone --filter=blob:none <url>    # partial clone (no file blobs initially)
git fetch --filter=blob:none
git fetch --filter=tree:0             # extreme, only commits initially


# ============================================================
# U) BUNDLES (offline sharing)
# ============================================================

git bundle create repo.bundle --all
git bundle verify repo.bundle
git clone repo.bundle <dir>
git fetch repo.bundle main


# ============================================================
# V) EMAIL / PATCH WORKFLOWS (common in OSS)
# ============================================================

git format-patch -1 <commit>
git format-patch <since>..<until>
git send-email *.patch                # requires config + sendmail setup
git am *.patch


# ============================================================
# W) SERVER / TRANSPORT (rare, but exists)
# ============================================================

git daemon --reuseaddr --base-path=.  # serve repos via git://
git instaweb                          # quick web view (depends tools)


# ============================================================
# X) FAST IMPORT/EXPORT (mass migration)
# ============================================================

git fast-export --all > out.fe
git fast-import < out.fe


# ============================================================
# Y) SUBTREE (alternative to submodules)
# ============================================================

git subtree add --prefix=<dir> <remote> <branch> --squash
git subtree pull --prefix=<dir> <remote> <branch> --squash
git subtree push --prefix=<dir> <remote> <branch>


# ============================================================
# Z) CONFIG KEYS (important ones you actually set)
# ============================================================

git config --global user.name "Name"
git config --global user.email "email"
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
git config --global core.autocrlf input
git config --global pull.rebase true
git config --global rebase.autoStash true
git config --global fetch.prune true
git config --global rerere.enabled true
git config --global commit.gpgsign true
git config --global tag.gpgsign true
git config --global gpg.program gpg
git config --global credential.helper cache


# ============================================================
# AA) ENV VARS (debug & behavior overrides)
# ============================================================

GIT_TRACE=1 git <cmd>
GIT_TRACE_PACKET=1 git <cmd>
GIT_TRACE_PERFORMANCE=1 git <cmd>
GIT_CURL_VERBOSE=1 git <cmd>

GIT_PAGER=cat git log
GIT_EDITOR=vim git commit
GIT_SSH_COMMAND="ssh -i key" git fetch


# ============================================================
# AB) ATTRIBUTES / EOL / DIFF DRIVERS (project-level)
# ============================================================

# .gitattributes examples:
# *.py text eol=lf
# *.png binary
# *.lock -diff
# *.md diff=markdown

git check-attr -a -- <file>


# ============================================================
# AC) IGNORE / EXCLUDE (three layers)
# ============================================================

# .gitignore            -> project ignore
# .git/info/exclude     -> local repo ignore (not committed)
# core.excludesfile     -> global ignore file

git config --global core.excludesfile ~/.config/git/ignore


# ============================================================
# AD) SIGNING / VERIFY (security)
# ============================================================

git log --show-signature
git verify-commit <commit>
git verify-tag <tag>
git commit -S -m "signed commit"
git tag -s v1.2 -m "signed tag"


# ============================================================
# AE) RARE BUT REAL COMMANDS (exist in many installs)
# ============================================================

git archive --remote=<url> HEAD > src.tar
git credential fill
git interpret-trailers --in-place <file>
git mailinfo
git mailsplit
