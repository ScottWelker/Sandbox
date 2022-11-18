[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Command Line Interface (CLI)](/Tech-Ref/CLI-\(Command-Line-Interface\)) | [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git)

[[_TOC_]]

---
# Introduction
While there are some great [git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git) [GUIs](/Tech-Ref/Software-Development/UX-\(User-Experience\)/GUI-\(Graphical-User-Interface\)) and [IDE](/Tech-Ref/Software-Development/IDE-\(Integrated-Development-Environment\)) integrations,  [I (SWelker)](/Individuals/Scott-Welker) learned to use [git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git) from the [command line](/Tech-Ref/CLI-\(Command-Line-Interface\)) and I continue to use it for almost everything.

## Reference
1. https://git-scm.com/docs/git
1. [Getting Started - The Command Line](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line)

---
# Topics
1. [Git](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/Git).

---
# Tips and Tricks

## Difference between 'git pull' and 'git fetch'?
- "_In the simplest terms, git pull does a git fetch followed by a git merge._"
   - [StackOverflow: Accepted Answer](https://stackoverflow.com/a/292359/418950).

## Find Deleted File
- [How to find a deleted file in the project commit history?](https://stackoverflow.com/q/7203515/418950)
   1. If you do not know the exact path you may use:
      - `git log --all --full-history -- "**/thefile.*"`
   1. If you know the path the file was at, you can do this:
      - `git log --all --full-history -- <path-to-file>`

## Reset to Remote Repository
|:warning: CAUTION!|
|:-|
|This discards uncommitted changes! As a rule you should avoid doing this. |

- [Setting your branch to exactly match the remote branch...](https://stackoverflow.com/a/1628334/418950)
```dos
git fetch origin
git reset --hard origin/master
```

## Undo possibilities in Git
As appropriate to your circumstances, execute the instructions under one or more of the following subsections.
- [Undo possibilities in Git](https://docs.gitlab.com/ee/topics/git/numerous_undo_possibilities_in_git/)
- [StackExchange: How do I revert all local changes](https://stackoverflow.com/a/1146981/418950)

#### Clean Untracked Files or Folders
- :+1: You may still have untracked files or folders that you'll want to clean out:
   - `git clean -f` (files)
   - `git clean -fd` (files and folders/directories)

#### Unstage a Local File
- :warning: **WARNING: This resets all unpushed commits!**
- To [unstage a local file](https://stackoverflow.com/a/348234/418950) that you mistakenly added (`git add <file?`) while preserving your local changes:
   - `git reset <file>` 
   - or simply `git reset`
   - :+1: You may still have untracked files or folders that you'll want to clean out. See [Clean Untracked Files or Folders](#clean-untracked-files-or-folders).

#### Overwrite Local Changes
1. To overwrite local changes:
   - `git checkout -- <file>`
   - or simply `git checkout .`
   - :+1: You may still have untracked files or folders that you'll want to clean out. See [Clean Untracked Files or Folders](#clean-untracked-files-or-folders).

#### Save Local Changes and Continue Working (stash --keep-index)
Stashing and keeping the index intact enables you to save your current work but continue working on that same code base. I found this useful when my code was ready to commit and push, representing an important milestone, but something kept me from being able to commit and push it. I needed to continue working from that point but retain the ability to return to it later to perform the "_clean commit_." 

The process unfolded like this:
1. At some milestone, code is ready but some external factor prevents commit/push at this time.
1. Ready the code as if you are going to commit/push it.
1. Stash it while keeping it in the index: `git stash -k -m"<some meaningful description>`.
1. Continue with whatever changes are needed to extend the saved, "_milestone code_" that you stashed (but kept in the index).
1. When the external factor that prevented commit/push is resolved, save your progress in another "_normal stash_": `git stash -m"<some meaningful description>"`.
   - :warning: Un-tested! Unsure how this is properly completed. I'll return here and update this based on experience.


#### Set Aside Local Changes to Work on Something Else (stash)
1. To set aside your local changes to work on something else:
   - `git stash`

#### Discard ALL local changes to all files.
1. To discard **ALL** local changes to all files, permanently:
   - `git reset --hard`
   - `git `
