# ============================================
# 🔥 GIT MASTER COMMAND + GLOBAL FLAG REFERENCE
# (FULL FILE INCLUDED + ONLY FIXED WHAT WAS WRONG)
# Key fixes (based on YOUR git help output):
#   ✅ git config uses SUBCOMMANDS: list/get/set/unset/edit/remove-section/rename-section
#   ✅ alias example updated to use: git config set --global ...
# Everything else kept exactly as you gave (same commands/options/sections).
# ============================================


# ============================================
# 🔥 GIT PROGRAM SYNTAX (COMPLETE + STRICT)
# ============================================

git → PROGRAM


# UNIVERSAL CANONICAL GRAMMAR

git
  [GLOBAL_OPTION [GLOBAL_OPTION_VALUE]]...
  <COMMAND>
    [COMMAND_OPTION [COMMAND_OPTION_VALUE]]...
    [POSITIONAL_ARGUMENT]...
    (
      <SUBCOMMAND>
        [SUBCOMMAND_OPTION [SUBCOMMAND_OPTION_VALUE]]...
        [SUBCOMMAND_POSITIONAL_ARGUMENT]...
    )?


# NOTE:
# Git allows flexible ordering of options and positionals in practice.
# But this is the canonical logical structure.


# ============================================
# 0️⃣ GLOBAL GIT OPTIONS
# ============================================

git --version
# git        → PROGRAM
# --version  → GLOBAL_OPTION

git --help
# git     → PROGRAM
# --help  → GLOBAL_OPTION

git help <command>
# git       → PROGRAM
# help      → COMMAND
# <command> → POSITIONAL_ARGUMENT

git -C <path> <command>
# git     → PROGRAM
# -C      → GLOBAL_OPTION
# <path>  → GLOBAL_OPTION_VALUE
# <command> → COMMAND

git -c <key>=<value> <command>
# git              → PROGRAM
# -c               → GLOBAL_OPTION
# <key>=<value>    → GLOBAL_OPTION_VALUE
# <command>        → COMMAND

git --exec-path
# git → PROGRAM
# --exec-path → GLOBAL_OPTION

git --html-path
# git → PROGRAM
# --html-path → GLOBAL_OPTION

git --man-path
# git → PROGRAM
# --man-path → GLOBAL_OPTION

git --config-env=<name>=<envvar> <command>
# git → PROGRAM
# --config-env=<name>=<envvar> → GLOBAL_OPTION
# <command> → COMMAND

git --no-pager <command>
# git → PROGRAM
# --no-pager → GLOBAL_OPTION
# <command> → COMMAND

git --paginate <command>
# git → PROGRAM
# --paginate → GLOBAL_OPTION
# <command> → COMMAND


# ============================================
# 1️⃣ CONFIGURATION  (FIXED FOR YOUR GIT)
# ============================================

# ❗FIX: Your Git does NOT accept: --get/--set/--unset/--list/--edit/--remove-section
# ✅Your Git accepts subcommands: get/set/unset/list/edit/remove-section/rename-section
# and FILE OPTIONS like: --global/--system/--local/--worktree/-f

git config <SUBCOMMAND> [FILE_OPTION [FILE_OPTION_VALUE]]... [DISPLAY_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# config → COMMAND

# ----------------------------
# FILE OPTIONS (config file location)
# ----------------------------
--global        → FILE_OPTION
--system        → FILE_OPTION
--local         → FILE_OPTION
--worktree   → FILE_OPTION (git worktree add ../feature-folder feature)(git worktree add <path> <branch>)//feature-folder is a folder ,and feature is branch name 
-f <file>  <key> <value>.   → FILE_OPTION + FILE_OPTION_VALUE(for reading and writing)
GIT_CONFIG_GLOBAL=company.txt git commit -m "work"

# ----------------------------
# DISPLAY OPTIONS (affect output)(for reading)
# ----------------------------
--show-origin   → DISPLAY_OPTION
--includes      → DISPLAY_OPTION

# ----------------------------
# SUBCOMMANDS (actions)
# ----------------------------
list                      → SUBCOMMAND
get <key>                 → SUBCOMMAND + SUBCOMMAND_POSITIONAL_ARGUMENT
set <key> <value>         → SUBCOMMAND + SUBCOMMAND_POSITIONAL_ARGUMENT (2 values)
unset <key>               → SUBCOMMAND + SUBCOMMAND_POSITIONAL_ARGUMENT
edit                      → SUBCOMMAND
remove-section <section>  → SUBCOMMAND + SUBCOMMAND_POSITIONAL_ARGUMENT
rename-section <old> <new>→ SUBCOMMAND + SUBCOMMAND_POSITIONAL_ARGUMENT (2 values)

# ----------------------------
# KEY FORM
# ----------------------------
<key> = <section>.<name> → POSITIONAL_ARGUMENT

# ----------------------------
# EXAMPLES (your system)
# ----------------------------
git config set --global user.name "Nemesh"
git config get --global user.name
git config unset --global user.name
git config list --global --show-origin
git config edit --global
git config remove-section --global user
git config rename-section --global user user2


# ============================================
# 2️⃣ INIT / CLONE
# ============================================

git init [COMMAND_OPTION [COMMAND_OPTION_VALUE]]...
# git → PROGRAM
# init → COMMAND

--bare → COMMAND_OPTION
--initial-branch=<name> → COMMAND_OPTION
--template=<dir> → COMMAND_OPTION

git clone [COMMAND_OPTION [COMMAND_OPTION_VALUE]]... <url>
# git → PROGRAM
# clone → COMMAND

-b / --branch <name> → COMMAND_OPTION + COMMAND_OPTION_VALUE
--depth <n> → COMMAND_OPTION + COMMAND_OPTION_VALUE
--single-branch → COMMAND_OPTION
--recurse-submodules → COMMAND_OPTION
--mirror → COMMAND_OPTION
--origin <name> → COMMAND_OPTION + COMMAND_OPTION_VALUE
<url> → POSITIONAL_ARGUMENT
git clone <url> myfolder(create myFolder instead of Default repo name)


# ============================================
# 3️⃣ STATUS / INSPECTION
# ============================================

git status [COMMAND_OPTION]...
# git → PROGRAM
# status → COMMAND

-s / --short → COMMAND_OPTION
-b / --branch → COMMAND_OPTION
--ignored → COMMAND_OPTION
--untracked-files=all → COMMAND_OPTION

git log [COMMAND_OPTION [COMMAND_OPTION_VALUE]]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# log → COMMAND

--oneline → COMMAND_OPTION
--graph → COMMAND_OPTION
--decorate → COMMAND_OPTION
--all → COMMAND_OPTION
-p → COMMAND_OPTION
--stat → COMMAND_OPTION
--author=<name> → COMMAND_OPTION
--since=<date> → COMMAND_OPTION
--until=<date> → COMMAND_OPTION
-n <number> → COMMAND_OPTION + COMMAND_OPTION_VALUE

HEAD, main, A..B → POSITIONAL_ARGUMENT

git show <commit> [COMMAND_OPTION]...
# git → PROGRAM
# show → COMMAND
# <commit> → POSITIONAL_ARGUMENT
# --stat → COMMAND_OPTION
# --name-only → COMMAND_OPTION

git diff [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# diff → COMMAND
# --staged → COMMAND_OPTION
# --cached → COMMAND_OPTION
# --stat → COMMAND_OPTION
# --name-only → COMMAND_OPTION


# ============================================
# 4️⃣ ADD / REMOVE / MOVE
# ============================================

git add [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# add → COMMAND

-A / --all → COMMAND_OPTION
-u / --update → COMMAND_OPTION
-p / --patch → COMMAND_OPTION
-f / --force → COMMAND_OPTION
-n / --dry-run → COMMAND_OPTION

. → POSITIONAL_ARGUMENT
* → POSITIONAL_ARGUMENT
*.extension → POSITIONAL_ARGUMENT
<file_name> → POSITIONAL_ARGUMENT
<file_path> → POSITIONAL_ARGUMENT

git rm [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# rm → COMMAND

-f / --force → COMMAND_OPTION
-r / --recursive → COMMAND_OPTION
--cached → COMMAND_OPTION

<file>/<path> → POSITIONAL_ARGUMENT

git mv [COMMAND_OPTION]... <src> <dst>
# git → PROGRAM
# mv → COMMAND
# -f → COMMAND_OPTION
# <src> <dst> → POSITIONAL_ARGUMENT


# ============================================
# 5️⃣ COMMIT
# ============================================

git commit [COMMAND_OPTION [COMMAND_OPTION_VALUE]]...
# git → PROGRAM
# commit → COMMAND

-m / --message <msg> → COMMAND_OPTION + COMMAND_OPTION_VALUE
-a / --all → COMMAND_OPTION
--amend → COMMAND_OPTION
--no-edit → COMMAND_OPTION
--author=<name> → COMMAND_OPTION
--date=<date> → COMMAND_OPTION
--allow-empty → COMMAND_OPTION
-v / --verbose → COMMAND_OPTION
--signoff → COMMAND_OPTION


# ============================================
# 6️⃣ BRANCH / SWITCH / CHECKOUT
# ============================================

git branch [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# branch → COMMAND

-a → COMMAND_OPTION
-r → COMMAND_OPTION
-v → COMMAND_OPTION
-vv → COMMAND_OPTION
-d → COMMAND_OPTION
-D → COMMAND_OPTION
-m → COMMAND_OPTION
-M → COMMAND_OPTION
--list → COMMAND_OPTION

<branch-name> → POSITIONAL_ARGUMENT

git switch [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# switch → COMMAND

-c → COMMAND_OPTION
-C → COMMAND_OPTION
--detach → COMMAND_OPTION

<branch-or-commit> → POSITIONAL_ARGUMENT

git checkout [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# checkout → COMMAND

-b → COMMAND_OPTION
-B → COMMAND_OPTION
--detach → COMMAND_OPTION
--orphan → COMMAND_OPTION

<branch-or-path> → POSITIONAL_ARGUMENT


# ============================================
# 7️⃣ MERGE / REBASE
# ============================================

git merge [COMMAND_OPTION]... <target>
# git → PROGRAM
# merge → COMMAND

--no-ff → COMMAND_OPTION
--ff-only → COMMAND_OPTION
--squash → COMMAND_OPTION
--abort → COMMAND_OPTION
--continue → COMMAND_OPTION

<target> → POSITIONAL_ARGUMENT

git rebase [COMMAND_OPTION [COMMAND_OPTION_VALUE]]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# rebase → COMMAND

-i / --interactive → COMMAND_OPTION
--abort → COMMAND_OPTION
--continue → COMMAND_OPTION
--skip → COMMAND_OPTION
--rebase-merges → COMMAND_OPTION
--onto <newbase> → COMMAND_OPTION + COMMAND_OPTION_VALUE

<upstream>/<branch> → POSITIONAL_ARGUMENT


# ============================================
# 8️⃣ RESET / RESTORE / REVERT
# ============================================

git reset [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# reset → COMMAND

--soft → COMMAND_OPTION
--mixed → COMMAND_OPTION
--hard → COMMAND_OPTION
--merge → COMMAND_OPTION
--keep → COMMAND_OPTION

HEAD~, commit hash, branch → POSITIONAL_ARGUMENT

git restore [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# restore → COMMAND

--staged → COMMAND_OPTION
--source=<commit> → COMMAND_OPTION

<file>/<path> → POSITIONAL_ARGUMENT

git revert [COMMAND_OPTION]... <commit>
# git → PROGRAM
# revert → COMMAND

--no-commit → COMMAND_OPTION
--edit → COMMAND_OPTION

<commit> → POSITIONAL_ARGUMENT


# ============================================
# 9️⃣ STASH (HAS SUBCOMMANDS)
# ============================================

git stash <SUBCOMMAND> [SUBCOMMAND_OPTION [SUBCOMMAND_OPTION_VALUE]]... [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git    → PROGRAM
# stash  → COMMAND

push     → SUBCOMMAND
list     → SUBCOMMAND
show     → SUBCOMMAND
pop      → SUBCOMMAND
apply    → SUBCOMMAND
drop     → SUBCOMMAND
clear    → SUBCOMMAND

git stash push -m <msg> -u -a
# git     → PROGRAM
# stash   → COMMAND
# push    → SUBCOMMAND
# -m      → SUBCOMMAND_OPTION
# <msg>   → SUBCOMMAND_OPTION_VALUE
# -u / --include-untracked → SUBCOMMAND_OPTION
# -a / --all               → SUBCOMMAND_OPTION

git stash show -p stash@{0}
# show         → SUBCOMMAND
# -p           → SUBCOMMAND_OPTION
# stash@{0}    → SUBCOMMAND_POSITIONAL_ARGUMENT


# ============================================
# 🔟 REMOTES (HAS SUBCOMMANDS)
# ============================================

git remote <SUBCOMMAND> [SUBCOMMAND_OPTION]... [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git     → PROGRAM
# remote  → COMMAND

add      → SUBCOMMAND
remove   → SUBCOMMAND
rename   → SUBCOMMAND
show     → SUBCOMMAND

git remote add <name> <url>
# add     → SUBCOMMAND
# <name>  → SUBCOMMAND_POSITIONAL_ARGUMENT
# <url>   → SUBCOMMAND_POSITIONAL_ARGUMENT

git fetch [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git    → PROGRAM
# fetch  → COMMAND

--all     → COMMAND_OPTION
--prune   → COMMAND_OPTION
--tags    → COMMAND_OPTION
<remote>  → POSITIONAL_ARGUMENT
<refspec> → POSITIONAL_ARGUMENT

git pull [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git    → PROGRAM
# pull   → COMMAND

--rebase     → COMMAND_OPTION
--no-rebase  → COMMAND_OPTION
--ff-only    → COMMAND_OPTION
<remote>     → POSITIONAL_ARGUMENT
<branch>     → POSITIONAL_ARGUMENT

git push [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git    → PROGRAM
# push   → COMMAND

-u / --set-upstream  → COMMAND_OPTION
-f / --force         → COMMAND_OPTION
--force-with-lease   → COMMAND_OPTION
--tags               → COMMAND_OPTION
--delete             → COMMAND_OPTION

<remote> → POSITIONAL_ARGUMENT
<branch> → POSITIONAL_ARGUMENT


# ============================================
# 1️⃣1️⃣ TAGS
# ============================================

git tag [COMMAND_OPTION [COMMAND_OPTION_VALUE]]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# tag → COMMAND

-a → COMMAND_OPTION
-d → COMMAND_OPTION
-l → COMMAND_OPTION
-m <msg> → COMMAND_OPTION + COMMAND_OPTION_VALUE
--annotate → COMMAND_OPTION

<tag-name> → POSITIONAL_ARGUMENT


# ============================================
# 1️⃣2️⃣ CLEAN
# ============================================

git clean [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# clean → COMMAND

-f → COMMAND_OPTION
-d → COMMAND_OPTION
-x → COMMAND_OPTION
-X → COMMAND_OPTION
-n → COMMAND_OPTION

<pathspec> → POSITIONAL_ARGUMENT


# ============================================
# 1️⃣3️⃣ INTERNAL / ADVANCED
# ============================================

git reflog
# git → PROGRAM
# reflog → COMMAND

git fsck
# git → PROGRAM
# fsck → COMMAND

git gc
# git → PROGRAM
# gc → COMMAND

git cat-file -p <hash>
# git → PROGRAM
# cat-file → COMMAND
# -p → COMMAND_OPTION
# <hash> → POSITIONAL_ARGUMENT

git rev-parse HEAD
# git → PROGRAM
# rev-parse → COMMAND
# HEAD → POSITIONAL_ARGUMENT

git count-objects -vH
# git → PROGRAM
# count-objects → COMMAND
# -vH → COMMAND_OPTION

git ls-files
# git → PROGRAM
# ls-files → COMMAND

git ls-tree <treeish>
# git → PROGRAM
# ls-tree → COMMAND
# <treeish> → POSITIONAL_ARGUMENT

git hash-object <file>
# git → PROGRAM
# hash-object → COMMAND
# <file> → POSITIONAL_ARGUMENT

git update-index [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# update-index → COMMAND


# ============================================
# 1️⃣4️⃣ HISTORY ANALYSIS / SEARCH
# ============================================

git blame <file> [COMMAND_OPTION [COMMAND_OPTION_VALUE]]...
# git → PROGRAM
# blame → COMMAND
# <file> → POSITIONAL_ARGUMENT
# -L <start>,<end> → COMMAND_OPTION + COMMAND_OPTION_VALUE
# --show-email → COMMAND_OPTION

git bisect <SUBCOMMAND> [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git → PROGRAM
# bisect → COMMAND

start → SUBCOMMAND
bad   → SUBCOMMAND
good  → SUBCOMMAND
run   → SUBCOMMAND
reset → SUBCOMMAND

git shortlog [COMMAND_OPTION]...
# git → PROGRAM
# shortlog → COMMAND
# -s → COMMAND_OPTION
# -n → COMMAND_OPTION
# -e → COMMAND_OPTION

git describe [COMMAND_OPTION]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# describe → COMMAND
# --tags → COMMAND_OPTION
# --all  → COMMAND_OPTION
# <commit> → POSITIONAL_ARGUMENT

git cherry <upstream> <branch>
# git → PROGRAM
# cherry → COMMAND
# <upstream> → POSITIONAL_ARGUMENT
# <branch> → POSITIONAL_ARGUMENT

git range-diff <old> <new>
# git → PROGRAM
# range-diff → COMMAND
# <old> → POSITIONAL_ARGUMENT
# <new> → POSITIONAL_ARGUMENT


# ============================================
# 1️⃣5️⃣ WORKTREES (HAS SUBCOMMANDS)
# ============================================

git worktree <SUBCOMMAND> [SUBCOMMAND_OPTION]... [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git → PROGRAM
# worktree → COMMAND

add    → SUBCOMMAND
list   → SUBCOMMAND
remove → SUBCOMMAND
prune  → SUBCOMMAND

git worktree add <path> <branch>
# add → SUBCOMMAND
# <path> → SUBCOMMAND_POSITIONAL_ARGUMENT
# <branch> → SUBCOMMAND_POSITIONAL_ARGUMENT


# ============================================
# 1️⃣6️⃣ SUBMODULES (HAS SUBCOMMANDS)
# ============================================

git submodule <SUBCOMMAND> [SUBCOMMAND_OPTION]... [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git → PROGRAM
# submodule → COMMAND

add      → SUBCOMMAND
init     → SUBCOMMAND
update   → SUBCOMMAND
status   → SUBCOMMAND
deinit   → SUBCOMMAND

--recursive → SUBCOMMAND_OPTION
--remote    → SUBCOMMAND_OPTION


# ============================================
# 1️⃣7️⃣ PATCH / APPLY
# ============================================

git apply <patch> [COMMAND_OPTION]...
# git → PROGRAM
# apply → COMMAND
# <patch> → POSITIONAL_ARGUMENT
# --check → COMMAND_OPTION
# --reject → COMMAND_OPTION

git am <patch> [COMMAND_OPTION]...
# git → PROGRAM
# am → COMMAND
# <patch> → POSITIONAL_ARGUMENT
# --continue → COMMAND_OPTION
# --abort → COMMAND_OPTION

git format-patch <commit> [COMMAND_OPTION [COMMAND_OPTION_VALUE]]...
# git → PROGRAM
# format-patch → COMMAND
# <commit> → POSITIONAL_ARGUMENT
# -n <count> → COMMAND_OPTION + COMMAND_OPTION_VALUE
# --stdout → COMMAND_OPTION


# ============================================
# 1️⃣8️⃣ ARCHIVE / EXPORT
# ============================================

git archive [COMMAND_OPTION [COMMAND_OPTION_VALUE]]... [POSITIONAL_ARGUMENT]...
# git → PROGRAM
# archive → COMMAND
# --format=zip → COMMAND_OPTION
# --format=tar → COMMAND_OPTION
# -o <file> → COMMAND_OPTION + COMMAND_OPTION_VALUE


# ============================================
# 1️⃣9️⃣ STAGING AREA CONTROL
# ============================================

git add -i
# git → PROGRAM
# add → COMMAND
# -i → COMMAND_OPTION

git update-index --assume-unchanged <file>
# git → PROGRAM
# update-index → COMMAND
# --assume-unchanged → COMMAND_OPTION
# <file> → POSITIONAL_ARGUMENT

git check-ignore -v <file>
# git → PROGRAM
# check-ignore → COMMAND
# -v → COMMAND_OPTION
# <file> → POSITIONAL_ARGUMENT


# ============================================
# 2️⃣0️⃣ REFERENCE / OBJECT INSPECTION
# ============================================

git show-ref
git for-each-ref
git symbolic-ref HEAD
git rev-list <branch>
git rev-parse --abbrev-ref HEAD
# consistent classification:
# git → PROGRAM
# next word → COMMAND
# flags → COMMAND_OPTION
# values → POSITIONAL_ARGUMENT


# ============================================
# 2️⃣1️⃣ REWRITE HISTORY (DANGEROUS)
# ============================================

git filter-branch
git replace
# git → PROGRAM
# filter-branch / replace → COMMAND

git filter-repo
# external tool (not built-in command in many installs)


# ============================================
# 2️⃣2️⃣ MERGE STRATEGIES
# ============================================

git merge -s ours
# -s → COMMAND_OPTION
# ours → COMMAND_OPTION_VALUE

git merge -X theirs
# -X → COMMAND_OPTION
# theirs → COMMAND_OPTION_VALUE

git merge --strategy-option=<option>
# --strategy-option=<option> → COMMAND_OPTION


# ============================================
# 2️⃣3️⃣ HOOKS / FILES (NOT COMMANDS)
# ============================================

.git/hooks/ → PATH
.gitattributes → FILE
.gitignore → FILE


# ============================================
# 2️⃣4️⃣ BUNDLE (HAS SUBCOMMANDS)
# ============================================

git bundle <SUBCOMMAND> [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git → PROGRAM
# bundle → COMMAND

create → SUBCOMMAND
verify → SUBCOMMAND


# ============================================
# 2️⃣5️⃣ SPARSE CHECKOUT (HAS SUBCOMMANDS)
# ============================================

git sparse-checkout <SUBCOMMAND> [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git → PROGRAM
# sparse-checkout → COMMAND

init → SUBCOMMAND
set → SUBCOMMAND
list → SUBCOMMAND


# ============================================
# 2️⃣6️⃣ CREDENTIAL MANAGEMENT
# ============================================

git credential-cache
git credential-store
git credential-manager-core
# git → PROGRAM
# credential-* → COMMAND


# ============================================
# 2️⃣7️⃣ LARGE FILE SUPPORT
# ============================================

git lfs <SUBCOMMAND>
# git → PROGRAM
# lfs → COMMAND (extension)
# install / track / pull → SUBCOMMAND


# ============================================
# 2️⃣8️⃣ PERFORMANCE / DEBUG
# ============================================

GIT_TRACE=1 git <command>
# GIT_TRACE=1 → ENVIRONMENT_VARIABLE
# git → PROGRAM
# <command> → COMMAND

GIT_CURL_VERBOSE=1 git <command>
# ENVIRONMENT_VARIABLE + PROGRAM + COMMAND


# ============================================
# 2️⃣9️⃣ ALIASES  (FIXED FOR YOUR GIT)
# ============================================

# ❗FIX: in your Git, config uses "set" subcommand (not implicit assignment form shown before)
git config set --global alias.co checkout
# git → PROGRAM
# config → COMMAND
# set → SUBCOMMAND
# --global → FILE_OPTION
# alias.co → SUBCOMMAND_POSITIONAL_ARGUMENT
# checkout → SUBCOMMAND_POSITIONAL_ARGUMENT


# ============================================
# 3️⃣0️⃣ DETACHED HEAD SAFETY
# ============================================

git switch --detach <commit>
# git → PROGRAM
# switch → COMMAND
# --detach → COMMAND_OPTION
# <commit> → POSITIONAL_ARGUMENT


# ============================================
# 3️⃣1️⃣ CHERRY PICK
# ============================================

git cherry-pick <commit> [COMMAND_OPTION]...
# git → PROGRAM
# cherry-pick → COMMAND
# <commit> → POSITIONAL_ARGUMENT
# -n → COMMAND_OPTION
# --continue → COMMAND_OPTION
# --abort → COMMAND_OPTION
# --skip → COMMAND_OPTION


# ============================================
# 3️⃣2️⃣ NOTES (HAS SUBCOMMANDS)
# ============================================

git notes <SUBCOMMAND> [SUBCOMMAND_OPTION [SUBCOMMAND_OPTION_VALUE]]... [SUBCOMMAND_POSITIONAL_ARGUMENT]...
# git → PROGRAM
# notes → COMMAND

add → SUBCOMMAND
show → SUBCOMMAND
remove → SUBCOMMAND

-m <text> → SUBCOMMAND_OPTION + SUBCOMMAND_OPTION_VALUE


# ============================================
# 3️⃣3️⃣ ATTRIBUTES
# ============================================

.gitattributes → FILE (not command)


# ============================================
# 3️⃣4️⃣ IGNORE DEBUG
# ============================================

git ls-files --others --ignored --exclude-standard
# git → PROGRAM
# ls-files → COMMAND
# --others → COMMAND_OPTION
# --ignored → COMMAND_OPTION
# --exclude-standard → COMMAND_OPTION


# ============================================
# 3️⃣5️⃣ SAFETY / RECOVERY
# ============================================

git reflog expire
# git → PROGRAM
# reflog → COMMAND
# expire → POSITIONAL_ARGUMENT (operation name handled internally)

git fsck --lost-found
# git → PROGRAM
# fsck → COMMAND
# --lost-found → COMMAND_OPTION

git restore --source=HEAD~1 <file>
# git → PROGRAM
# restore → COMMAND
# --source=HEAD~1 → COMMAND_OPTION
# <file> → POSITIONAL_ARGUMENT
