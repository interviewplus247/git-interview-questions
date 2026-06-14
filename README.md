# Git Interview Questions & Answers

> A curated list of Git interview questions covering Fundamentals, Repository Management, Staging & Committing, Branching, Merging, Rebasing, Undoing Changes, Remote Repositories, Stashing, Tags & Releases, Git Internals, Workflows & Best Practices, and Advanced/Scenario-Based Questions — each with a clear explanation and command examples where applicable.

---

### Table of Contents

<details open>
<summary>
Hide/Show table of contents
</summary>

| No. | Questions |
| --- | --------- |
|     | **Git Fundamentals** |
| 1 | [What is Git?](#what-is-git) |
| 2 | [How is Git different from other version control systems?](#how-is-git-different-from-other-version-control-systems) |
| 3 | [What are the advantages of using Git?](#what-are-the-advantages-of-using-git) |
| 4 | [What is a repository in Git?](#what-is-a-repository-in-git) |
| 5 | [What is the difference between a local and a remote repository?](#what-is-the-difference-between-a-local-and-a-remote-repository) |
| 6 | [What are the three states of a file in Git?](#what-are-the-three-states-of-a-file-in-git) |
| 7 | [Describe the typical Git workflow.](#describe-the-typical-git-workflow) |
| 8 | [What is the .git directory?](#what-is-the-git-directory) |
| 9 | [How does Git store data internally?](#how-does-git-store-data-internally) |
| 10 | [What is a commit in Git?](#what-is-a-commit-in-git) |
| 11 | [What is a SHA-1 hash in Git?](#what-is-a-sha-1-hash-in-git) |
| 12 | [How does Git differ from GitHub?](#how-does-git-differ-from-github) |
| 13 | [What is GitLab and how does it differ from GitHub?](#what-is-gitlab-and-how-does-it-differ-from-github) |
| 14 | [List some basic Git commands every developer should know.](#list-some-basic-git-commands-every-developer-should-know) |
| 15 | [How do you initialize a new Git repository?](#how-do-you-initialize-a-new-git-repository) |
|     | **Repository Management** |
| 16 | [How do you clone an existing repository?](#how-do-you-clone-an-existing-repository) |
| 17 | [What is the difference between git init and git clone?](#what-is-the-difference-between-git-init-and-git-clone) |
| 18 | [How do you add a remote repository?](#how-do-you-add-a-remote-repository) |
| 19 | [How do you view configured remote repositories?](#how-do-you-view-configured-remote-repositories) |
| 20 | [How do you change a remote repository URL?](#how-do-you-change-a-remote-repository-url) |
| 21 | [How do you remove a remote repository?](#how-do-you-remove-a-remote-repository) |
| 22 | [How do you rename a Git remote?](#how-do-you-rename-a-git-remote) |
| 23 | [What is the purpose of git config?](#what-is-the-purpose-of-git-config) |
| 24 | [What are local, global and system configurations?](#what-are-local-global-and-system-configurations) |
| 25 | [How do you verify Git configuration settings?](#how-do-you-verify-git-configuration-settings) |
|     | **Staging and Committing** |
| 26 | [What is the staging area in Git?](#what-is-the-staging-area-in-git) |
| 27 | [Why is the staging area important?](#why-is-the-staging-area-important) |
| 28 | [What is the difference between git add . and git add -A?](#what-is-the-difference-between-git-add--and-git-add--a) |
| 29 | [What does git commit do?](#what-does-git-commit-do) |
| 30 | [What is the difference between git commit and git commit --amend?](#what-is-the-difference-between-git-commit-and-git-commit---amend) |
| 31 | [How do you modify the last commit message?](#how-do-you-modify-the-last-commit-message) |
| 32 | [What happens if you commit without staging files?](#what-happens-if-you-commit-without-staging-files) |
| 33 | [How do you commit only specific files?](#how-do-you-commit-only-specific-files) |
| 34 | [What are atomic commits?](#what-are-atomic-commits) |
| 35 | [Why should commits be small and meaningful?](#why-should-commits-be-small-and-meaningful) |
| 36 | [What is a commit hash?](#what-is-a-commit-hash) |
| 37 | [How do you view commit history?](#how-do-you-view-commit-history) |
| 38 | [How do you view changes before committing?](#how-do-you-view-changes-before-committing) |
| 39 | [How do you compare staged and unstaged changes?](#how-do-you-compare-staged-and-unstaged-changes) |
| 40 | [How do you undo a staged file?](#how-do-you-undo-a-staged-file) |
|     | **Branching** |
| 41 | [What is a branch in Git?](#what-is-a-branch-in-git) |
| 42 | [Why are branches used?](#why-are-branches-used) |
| 43 | [How do you create a new branch?](#how-do-you-create-a-new-branch) |
| 44 | [How do you switch between branches?](#how-do-you-switch-between-branches) |
| 45 | [What is the difference between git checkout and git switch?](#what-is-the-difference-between-git-checkout-and-git-switch) |
| 46 | [How do you create and switch to a branch in one command?](#how-do-you-create-and-switch-to-a-branch-in-one-command) |
| 47 | [What is the HEAD pointer in Git?](#what-is-the-head-pointer-in-git) |
| 48 | [What happens when you create a branch?](#what-happens-when-you-create-a-branch) |
| 49 | [How do you rename a branch?](#how-do-you-rename-a-branch) |
| 50 | [How do you delete a branch?](#how-do-you-delete-a-branch) |
| 51 | [What is a detached HEAD state?](#what-is-a-detached-head-state) |
| 52 | [How do you recover from a detached HEAD state?](#how-do-you-recover-from-a-detached-head-state) |
| 53 | [What are long-lived branches?](#what-are-long-lived-branches) |
| 54 | [What are short-lived feature branches?](#what-are-short-lived-feature-branches) |
| 55 | [What are branch naming conventions?](#what-are-branch-naming-conventions) |
|     | **Merging** |
| 56 | [What is Git merge?](#what-is-git-merge) |
| 57 | [What are the different types of merges?](#what-are-the-different-types-of-merges) |
| 58 | [What is a fast-forward merge?](#what-is-a-fast-forward-merge) |
| 59 | [What is a three-way merge?](#what-is-a-three-way-merge) |
| 60 | [What is a merge commit?](#what-is-a-merge-commit) |
| 61 | [How do you merge one branch into another?](#how-do-you-merge-one-branch-into-another) |
| 62 | [What is a merge conflict?](#what-is-a-merge-conflict) |
| 63 | [Why do merge conflicts occur?](#why-do-merge-conflicts-occur) |
| 64 | [How do you resolve merge conflicts?](#how-do-you-resolve-merge-conflicts) |
| 65 | [What tools can be used to resolve merge conflicts?](#what-tools-can-be-used-to-resolve-merge-conflicts) |
| 66 | [How do you abort a merge operation?](#how-do-you-abort-a-merge-operation) |
| 67 | [How do you view merge history?](#how-do-you-view-merge-history) |
| 68 | [What are merge strategies in Git?](#what-are-merge-strategies-in-git) |
| 69 | [What is an octopus merge?](#what-is-an-octopus-merge) |
| 70 | [What are the disadvantages of frequent merging?](#what-are-the-disadvantages-of-frequent-merging) |
|     | **Rebasing** |
| 71 | [What is Git rebase?](#what-is-git-rebase) |
| 72 | [How is rebase different from merge?](#how-is-rebase-different-from-merge) |
| 73 | [When should you use rebase?](#when-should-you-use-rebase) |
| 74 | [What is interactive rebase?](#what-is-interactive-rebase) |
| 75 | [How do you squash commits using rebase?](#how-do-you-squash-commits-using-rebase) |
| 76 | [What is commit squashing?](#what-is-commit-squashing) |
| 77 | [What are the benefits of rebasing?](#what-are-the-benefits-of-rebasing) |
| 78 | [What are the risks of rebasing shared branches?](#what-are-the-risks-of-rebasing-shared-branches) |
| 79 | [How do you resolve conflicts during rebase?](#how-do-you-resolve-conflicts-during-rebase) |
| 80 | [How do you continue a rebase after conflict resolution?](#how-do-you-continue-a-rebase-after-conflict-resolution) |
| 81 | [How do you abort a rebase?](#how-do-you-abort-a-rebase) |
| 82 | [What is the difference between rebase and rebase --interactive?](#what-is-the-difference-between-rebase-and-rebase---interactive) |
| 83 | [What is upstream in rebase?](#what-is-upstream-in-rebase) |
| 84 | [How do you rebase a feature branch onto main?](#how-do-you-rebase-a-feature-branch-onto-main) |
| 85 | [What are best practices for rebasing?](#what-are-best-practices-for-rebasing) |
|     | **Undoing Changes** |
| 86 | [How do you undo uncommitted changes?](#how-do-you-undo-uncommitted-changes) |
| 87 | [What is the difference between reset, revert and restore?](#what-is-the-difference-between-reset-revert-and-restore) |
| 88 | [What is git restore?](#what-is-git-restore) |
| 89 | [What is git reset?](#what-is-git-reset) |
| 90 | [What is the difference between soft, mixed and hard reset?](#what-is-the-difference-between-soft-mixed-and-hard-reset) |
| 91 | [When should you use a soft reset?](#when-should-you-use-a-soft-reset) |
| 92 | [When should you use a hard reset?](#when-should-you-use-a-hard-reset) |
| 93 | [What is git revert?](#what-is-git-revert) |
| 94 | [Why is revert preferred in shared repositories?](#why-is-revert-preferred-in-shared-repositories) |
| 95 | [How do you revert multiple commits?](#how-do-you-revert-multiple-commits) |
| 96 | [How do you undo the last commit without losing changes?](#how-do-you-undo-the-last-commit-without-losing-changes) |
| 97 | [How do you remove a file from a commit?](#how-do-you-remove-a-file-from-a-commit) |
| 98 | [How do you recover deleted commits?](#how-do-you-recover-deleted-commits) |
| 99 | [What is the Git reflog?](#what-is-the-git-reflog) |
| 100 | [How does reflog help in recovery scenarios?](#how-does-reflog-help-in-recovery-scenarios) |
|     | **Remote Repositories** |
| 101 | [What is a remote repository?](#what-is-a-remote-repository) |
| 102 | [What is the difference between git fetch and git pull?](#what-is-the-difference-between-git-fetch-and-git-pull) |
| 103 | [What does git fetch do?](#what-does-git-fetch-do) |
| 104 | [What does git pull do?](#what-does-git-pull-do) |
| 105 | [What is the difference between pull and merge?](#what-is-the-difference-between-pull-and-merge) |
| 106 | [How do you push changes to a remote repository?](#how-do-you-push-changes-to-a-remote-repository) |
| 107 | [What is force push?](#what-is-force-push) |
| 108 | [When is force push dangerous?](#when-is-force-push-dangerous) |
| 109 | [What is git push --force-with-lease?](#what-is-git-push---force-with-lease) |
| 110 | [What is upstream tracking?](#what-is-upstream-tracking) |
| 111 | [How do you set an upstream branch?](#how-do-you-set-an-upstream-branch) |
| 112 | [How do you view remote branches?](#how-do-you-view-remote-branches) |
| 113 | [How do you delete a remote branch?](#how-do-you-delete-a-remote-branch) |
| 114 | [What are remote tracking branches?](#what-are-remote-tracking-branches) |
| 115 | [What happens when multiple developers push simultaneously?](#what-happens-when-multiple-developers-push-simultaneously) |
|     | **Stashing** |
| 116 | [What is Git stash?](#what-is-git-stash) |
| 117 | [When should you use stash?](#when-should-you-use-stash) |
| 118 | [How do you create a stash?](#how-do-you-create-a-stash) |
| 119 | [How do you list available stashes?](#how-do-you-list-available-stashes) |
| 120 | [How do you apply a stash?](#how-do-you-apply-a-stash) |
| 121 | [What is the difference between git stash apply and git stash pop?](#what-is-the-difference-between-git-stash-apply-and-git-stash-pop) |
| 122 | [How do you delete a stash?](#how-do-you-delete-a-stash) |
| 123 | [Can untracked files be stashed?](#can-untracked-files-be-stashed) |
|     | **Tags and Releases** |
| 124 | [What is a tag in Git?](#what-is-a-tag-in-git) |
| 125 | [What is the difference between lightweight and annotated tags?](#what-is-the-difference-between-lightweight-and-annotated-tags) |
| 126 | [How do you create a tag?](#how-do-you-create-a-tag) |
| 127 | [How do you push tags to a remote repository?](#how-do-you-push-tags-to-a-remote-repository) |
| 128 | [How do you delete a tag?](#how-do-you-delete-a-tag) |
| 129 | [Why are tags important in release management?](#why-are-tags-important-in-release-management) |
| 130 | [How do teams use tags in CI/CD pipelines?](#how-do-teams-use-tags-in-cicd-pipelines) |
|     | **Git Internals** |
| 131 | [How does Git store objects internally?](#how-does-git-store-objects-internally) |
| 132 | [What are blob objects in Git?](#what-are-blob-objects-in-git) |
| 133 | [What are tree objects in Git?](#what-are-tree-objects-in-git) |
| 134 | [What are commit objects in Git?](#what-are-commit-objects-in-git) |
| 135 | [What are tag objects in Git?](#what-are-tag-objects-in-git) |
| 136 | [What is the Git object database?](#what-is-the-git-object-database) |
| 137 | [What is packfile compression?](#what-is-packfile-compression) |
| 138 | [How does Git achieve high performance?](#how-does-git-achieve-high-performance) |
|     | **Git Workflows & Best Practices** |
| 139 | [What is Git Flow?](#what-is-git-flow) |
| 140 | [What is GitHub Flow?](#what-is-github-flow) |
| 141 | [What is GitLab Flow?](#what-is-gitlab-flow) |
| 142 | [What is Trunk-Based Development?](#what-is-trunk-based-development) |
| 143 | [Which Git workflow is most suitable for Agile teams?](#which-git-workflow-is-most-suitable-for-agile-teams) |
| 144 | [How do you handle hotfixes in Git?](#how-do-you-handle-hotfixes-in-git) |
| 145 | [What branching strategy do you follow in your current project?](#what-branching-strategy-do-you-follow-in-your-current-project) |
| 146 | [How do you review code using pull requests?](#how-do-you-review-code-using-pull-requests) |
| 147 | [What Git best practices do you follow in large teams?](#what-git-best-practices-do-you-follow-in-large-teams) |
| 148 | [How do you maintain a clean commit history?](#how-do-you-maintain-a-clean-commit-history) |
| 149 | [How do you handle release branches in production systems?](#how-do-you-handle-release-branches-in-production-systems) |
| 150 | [What are the most common Git mistakes and how can they be avoided?](#what-are-the-most-common-git-mistakes-and-how-can-they-be-avoided) |
|     | **Advanced & Scenario-Based Questions** |
| 151 | [What is git cherry-pick and when do you use it?](#what-is-git-cherry-pick-and-when-do-you-use-it) |
| 152 | [What is the difference between git reset and git checkout for files?](#what-is-the-difference-between-git-reset-and-git-checkout-for-files) |
| 153 | [What is git bisect and how does it help debug?](#what-is-git-bisect-and-how-does-it-help-debug) |
| 154 | [What are Git hooks?](#what-are-git-hooks) |
| 155 | [What is the difference between a fork and a clone?](#what-is-the-difference-between-a-fork-and-a-clone) |
| 156 | [What are Git submodules?](#what-are-git-submodules) |
| 157 | [What is git worktree?](#what-is-git-worktree) |
| 158 | [What is the difference between git merge --squash and interactive squash?](#what-is-the-difference-between-git-merge---squash-and-interactive-squash) |
| 159 | [How do you find who changed a line of code?](#how-do-you-find-who-changed-a-line-of-code) |
| 160 | [How would you remove sensitive data committed to a repository?](#how-would-you-remove-sensitive-data-committed-to-a-repository) |
| 161 | [What is a shallow clone and when is it useful?](#what-is-a-shallow-clone-and-when-is-it-useful) |
| 162 | [How do you handle a large binary file in Git?](#how-do-you-handle-a-large-binary-file-in-git) |
| 163 | [What is the difference between HEAD, working tree, and index?](#what-is-the-difference-between-head-working-tree-and-index) |
| 164 | [How do you resolve "your branch has diverged" errors?](#how-do-you-resolve-your-branch-has-diverged-errors) |
| 165 | [How would you undo a pushed commit on a shared branch?](#how-would-you-undo-a-pushed-commit-on-a-shared-branch) |

</details>

---

## Git Fundamentals

1. ### What is Git?

   **Git** is a **distributed version control system (DVCS)** designed to track changes in files and coordinate work among multiple developers. A Git repository is essentially a database of **snapshots** of your project. Unlike centralized version control systems, every clone of a Git repository contains the **full history**, enabling offline work and powerful branching and merging capabilities.

   Git was created by **Linus Torvalds in 2005** to manage Linux kernel development after the project lost access to its proprietary VCS. Its design goals were speed, data integrity, and support for distributed, non-linear workflows.

   ```bash
   # Initialize a new repository and make your first commit
   git init
   echo "# My Project" > README.md
   git add README.md
   git commit -m "Initial commit"
   ```

   **[⬆ Back to Top](#table-of-contents)**

2. ### How is Git different from other version control systems?

   Git differs from systems like Subversion (SVN) or Mercurial in several ways:

   - **Distributed architecture** — every clone has a complete history, so developers can commit, branch, and inspect history without network access.
   - **Snapshot-based storage** — Git stores content as snapshots of the entire directory tree rather than tracking individual deltas. Each commit represents the full state of the repository at that point.
   - **Content integrity** — objects are identified by SHA-1 (or SHA-256) hashes, ensuring data cannot be silently corrupted.
   - **Speed and efficiency** — operations such as branching and merging are fast because branches are just pointers to commits.
   - **Staging area** — Git introduces an **index (staging area)** where changes are prepared before committing; the commit records only what is in the staging area.

   | Feature | Git | SVN (centralized) |
   | --- | --- | --- |
   | History location | Every clone | Central server only |
   | Offline commits | ✅ | ❌ |
   | Branching cost | Cheap (pointer) | Expensive (server copy) |
   | Storage model | Snapshots | Deltas |
   | Integrity | SHA hashing | Revision numbers |

   **[⬆ Back to Top](#table-of-contents)**

3. ### What are the advantages of using Git?

   - **Local commits** — commits happen locally and can be pushed later, making work independent of network connectivity.
   - **Cheap branching and merging** — developers can create feature branches quickly, experiment, and merge without affecting others.
   - **Integrity and security** — every object is checksummed; Git detects corruption automatically.
   - **Flexibility** — supports multiple workflows (Git Flow, GitHub Flow, trunk-based development) and integrates with many hosting providers.
   - **Large ecosystem** — GitHub, GitLab, and Bitbucket provide collaboration features such as pull requests and CI/CD.

   **[⬆ Back to Top](#table-of-contents)**

4. ### What is a repository in Git?

   A **repository (repo)** is a collection of files tracked by Git. It contains three key parts:

   - **Working directory** — the checked-out version of your project that you edit.
   - **Index (staging area)** — a file that records what will go into the next commit.
   - **Object database** — Git's `.git` directory, which stores all objects (commits, trees, blobs, tags) and references.

   ```bash
   # The .git folder IS the repository; everything else is your working tree
   ls -a
   # .git  README.md  src/  ...
   ```

   **[⬆ Back to Top](#table-of-contents)**

5. ### What is the difference between a local and a remote repository?

   - A **local repository** is the `.git` directory in your project. It contains the complete history and branches and lives on your machine.
   - A **remote repository** is a hosted version of the repository (e.g., on GitHub, GitLab, or a self-hosted server). Remotes facilitate collaboration by allowing multiple users to push and pull changes.

   ```bash
   # Local repo created by init/clone; remote is a named reference (e.g. origin)
   git remote -v
   # origin  https://github.com/user/repo.git (fetch)
   # origin  https://github.com/user/repo.git (push)
   ```

   **[⬆ Back to Top](#table-of-contents)**

6. ### What are the three states of a file in Git?

   Every tracked file exists in one of three states:

   - **Modified** — you have changed the file in your working directory but haven't staged it.
   - **Staged** — the file is added to the index via `git add`. Only staged changes go into the next commit.
   - **Committed** — the snapshot is safely stored in the repository history.

   These map to the three areas of Git: the **working directory**, the **staging area**, and the **.git repository**.

   ```bash
   git status
   # modified:   app.js     (not staged)
   git add app.js           # → staged
   git commit -m "Update"   # → committed
   ```

   **[⬆ Back to Top](#table-of-contents)**

7. ### Describe the typical Git workflow.

   The basic workflow involves four steps:

   1. **Modify files** — make changes in your working directory.
   2. **Stage changes** — use `git add <file>` or `git add .` to add changes to the staging area.
   3. **Commit** — run `git commit -m "message"` to record a snapshot of the staged changes.
   4. **Push/Pull** — sync your local repository with a remote using `git push` and `git pull`.

   ```bash
   git add .
   git commit -m "Add login feature"
   git pull --rebase origin main   # integrate others' work first
   git push origin main
   ```

   **[⬆ Back to Top](#table-of-contents)**

8. ### What is the .git directory?

   When you initialize a repository with `git init`, Git creates a hidden **`.git` folder**. It contains the object database, references (branches and tags), configuration, and hooks. Manipulating files in `.git` manually is discouraged; commands like `git status` and `git branch` provide safe interfaces.

   ```
   .git/
     HEAD            ← points to the current branch
     config          ← repository-level configuration
     objects/        ← the object database (blobs, trees, commits, tags)
     refs/
       heads/        ← local branches
       tags/         ← tags
     hooks/          ← client/server-side hook scripts
     index           ← the staging area
   ```

   **[⬆ Back to Top](#table-of-contents)**

9. ### How does Git store data internally?

   Git stores data as **objects**: **blobs** (file contents), **trees** (directory listings), **commits** (snapshots with metadata), and **tags**. Each object is identified by a **SHA-1 hash** of its content. Commits reference a tree object and parent commits, forming a **directed acyclic graph (DAG)**. This design makes the entire history tamper-evident — changing any byte changes the hash.

   ```bash
   # Inspect the type and content of any object by its hash
   git cat-file -t 4b825dc   # → commit / tree / blob
   git cat-file -p HEAD      # → shows tree, parent, author, message
   ```

   **[⬆ Back to Top](#table-of-contents)**

10. ### What is a commit in Git?

    A **commit** records a snapshot of the project at a specific point in time. It contains:

    - A **tree object** representing the state of the directory tree.
    - **Metadata** — author, committer, timestamps, and the commit message.
    - **Parent references** — one parent for normal commits; two or more for merge commits.
    - A **SHA-1 hash** that uniquely identifies the commit.

    ```bash
    git commit -m "Fix null pointer in checkout flow"
    git show --stat HEAD   # view the commit's metadata and changed files
    ```

    **[⬆ Back to Top](#table-of-contents)**

11. ### What is a SHA-1 hash in Git?

    Git uses cryptographic hashes (**SHA-1**, or **SHA-256** in newer versions) to identify objects. The hash is computed from an object's **type, size, and content**. If any content changes, the hash changes — guaranteeing integrity. References like `HEAD` and branches ultimately store these hashes.

    A full hash is 40 hexadecimal characters; Git lets you use a unique abbreviation (often 7 characters):

    ```bash
    git log --oneline
    # a1b2c3d  Add user authentication
    git show a1b2c3d   # the short hash works as long as it's unambiguous
    ```

    **[⬆ Back to Top](#table-of-contents)**

12. ### How does Git differ from GitHub?

    **Git** is the version control system — a command-line tool that runs locally. **GitHub** is a **hosting service** that stores Git repositories in the cloud and adds collaboration features (issues, pull requests, code review, CI/CD via GitHub Actions). You can use Git entirely without GitHub, and you can host Git repos on other services like GitLab, Bitbucket, or a self-hosted server.

    | | Git | GitHub |
    | --- | --- | --- |
    | What it is | Version control tool | Hosting + collaboration platform |
    | Runs | Locally | In the cloud |
    | Required | Yes (to use Git) | No (optional) |

    **[⬆ Back to Top](#table-of-contents)**

13. ### What is GitLab and how does it differ from GitHub?

    **GitLab** is another Git hosting platform. While GitHub historically focused on code hosting and collaboration, **GitLab integrates CI/CD pipelines, issue tracking, and DevOps tooling into a single platform** out of the box. GitHub offers similar capabilities via GitHub Actions and its broader marketplace, but GitLab emphasizes a built-in, end-to-end DevOps experience. Both are excellent; the choice often depends on team preference and existing tooling.

    **[⬆ Back to Top](#table-of-contents)**

14. ### List some basic Git commands every developer should know.

    | Command | Purpose |
    | --- | --- |
    | `git init` | Create a new repository |
    | `git clone <url>` | Copy an existing repository |
    | `git status` | View working directory and staged file status |
    | `git add` | Add files to the staging area |
    | `git commit` | Record staged changes in history |
    | `git log` | View commit history |
    | `git branch` | List, create, or delete branches |
    | `git checkout` / `git switch` | Switch branches or restore files |
    | `git merge` | Merge another branch into the current branch |
    | `git pull` | Fetch and integrate changes from a remote |
    | `git push` | Push local commits to a remote |

    **[⬆ Back to Top](#table-of-contents)**

15. ### How do you initialize a new Git repository?

    Use `git init` in the project directory. This creates a `.git` directory and prepares the repository. Alternatively, clone an existing repository with `git clone <url>`.

    ```bash
    mkdir my-project && cd my-project
    git init
    # Initialized empty Git repository in /path/my-project/.git/

    # Optionally set the default branch name
    git init -b main
    ```

    **[⬆ Back to Top](#table-of-contents)**


## Repository Management

16. ### How do you clone an existing repository?

    Run `git clone <repository-URL>`. Git copies the entire history into a new directory and sets up a remote named `origin` pointing to the source. You can specify a custom directory name:

    ```bash
    git clone https://github.com/user/repo.git
    git clone https://github.com/user/repo.git my-project   # custom folder name
    git clone --branch develop https://github.com/user/repo.git  # clone a specific branch
    ```

    **[⬆ Back to Top](#table-of-contents)**

17. ### What is the difference between git init and git clone?

    - **`git init`** initializes a new, empty repository with no history. It sets up a `.git` folder but doesn't fetch any remote data.
    - **`git clone`** creates a copy of an existing repository, checks out its latest files, and configures a remote named `origin`.

    Use `git init` to start a brand-new project; use `git clone` to begin working on an existing one.

    **[⬆ Back to Top](#table-of-contents)**

18. ### How do you add a remote repository?

    Use `git remote add <name> <url>`:

    ```bash
    git remote add origin https://github.com/user/repo.git
    # You can add multiple remotes (e.g., a fork's upstream)
    git remote add upstream https://github.com/original/repo.git
    ```

    You can then push to and fetch from that remote by name.

    **[⬆ Back to Top](#table-of-contents)**

19. ### How do you view configured remote repositories?

    Use `git remote -v`. It shows the remotes and their fetch/push URLs:

    ```bash
    git remote -v
    # origin    https://github.com/user/repo.git (fetch)
    # origin    https://github.com/user/repo.git (push)
    # upstream  https://github.com/original/repo.git (fetch)
    # upstream  https://github.com/original/repo.git (push)
    ```

    **[⬆ Back to Top](#table-of-contents)**

20. ### How do you change a remote repository URL?

    Use `git remote set-url <name> <new-url>`. A common case is switching from HTTPS to SSH:

    ```bash
    git remote set-url origin git@github.com:user/repo.git
    git remote -v   # verify the change
    ```

    **[⬆ Back to Top](#table-of-contents)**

21. ### How do you remove a remote repository?

    Use `git remote remove <name>` (or the older `git remote rm <name>`). This removes the reference from your local configuration — it does **not** delete the remote repository on the server.

    ```bash
    git remote remove upstream
    ```

    **[⬆ Back to Top](#table-of-contents)**

22. ### How do you rename a Git remote?

    To rename a **local remote reference**, use `git remote rename <oldName> <newName>`:

    ```bash
    git remote rename origin github
    ```

    To rename the actual **project on a hosting service** (GitHub, GitLab), use their web UI or API — Git itself cannot rename the server-side repository.

    **[⬆ Back to Top](#table-of-contents)**

23. ### What is the purpose of git config?

    `git config` manages Git configuration settings. Config values can be set at three levels, each overriding the broader one:

    - **System** (`--system`) — applies to every user on the computer.
    - **Global** (`--global`) — applies to your user account. Use this for your name and email.
    - **Local** (`--local`, the default) — applies to the current repository and overrides global and system settings.

    ```bash
    git config --global user.name  "Amandeep Dhillon"
    git config --global user.email "dev@example.com"
    git config --local  core.autocrlf input   # repo-specific override
    ```

    **[⬆ Back to Top](#table-of-contents)**

24. ### What are local, global and system configurations?

    | Scope | File location | Applies to |
    | --- | --- | --- |
    | **Local** | `.git/config` | The current repository (highest priority) |
    | **Global** | `~/.gitconfig` | All repos for the current user |
    | **System** | `/etc/gitconfig` | Every user on the machine (lowest priority) |

    When a setting exists at multiple levels, the **most specific (local) wins**.

    **[⬆ Back to Top](#table-of-contents)**

25. ### How do you verify Git configuration settings?

    Use `git config --list` to view all active values. To view a specific value, use `git config <section.key>`. Add a scope flag to inspect a particular level:

    ```bash
    git config --list                 # all effective settings
    git config user.email             # a single value
    git config --global --list        # only global settings
    git config --show-origin user.name  # shows which file the value came from
    ```

    **[⬆ Back to Top](#table-of-contents)**


## Staging and Committing

26. ### What is the staging area in Git?

    The **staging area (index)** is an intermediate buffer between the working directory and the commit history. When you run `git add`, the selected changes are recorded in the index. The next commit uses the index snapshot as its content. This design lets you craft commits containing **precisely** the changes you want.

    ```
    Working Directory  →  git add  →  Staging Area (Index)  →  git commit  →  Repository
    ```

    **[⬆ Back to Top](#table-of-contents)**

27. ### Why is the staging area important?

    The staging area provides **fine-grained control** over what goes into each commit. You can stage some modifications and leave others unstaged, enabling smaller, focused commits. Without a staging area, you would be forced to commit all modified files together or rely on separate per-file commands. This is what makes **atomic, reviewable commits** possible.

    ```bash
    git add -p   # interactively stage individual hunks within files
    ```

    **[⬆ Back to Top](#table-of-contents)**

28. ### What is the difference between git add . and git add -A?

    - **`git add .`** stages modified and new files in the current directory and its subdirectories. In modern Git it also stages deletions within that path.
    - **`git add -A`** (or `git add --all`) stages **all** changes across the **entire repository** — modifications, new files, and deletions — regardless of your current directory.

    The key distinction is **scope**: `.` is path-limited to where you are; `-A` covers the whole working tree.

    ```bash
    git add .     # changes under the current directory
    git add -A    # every change in the whole repo
    ```

    **[⬆ Back to Top](#table-of-contents)**

29. ### What does git commit do?

    `git commit` creates a new **commit object**. It captures the staged snapshot and records metadata (author, committer, message). After committing, `HEAD` moves to the new commit. Supply a message with `-m`, or omit it to open your editor.

    ```bash
    git commit -m "Add password validation"
    git commit              # opens editor for a multi-line message
    ```

    **[⬆ Back to Top](#table-of-contents)**

30. ### What is the difference between git commit and git commit --amend?

    `git commit --amend` **modifies the most recent commit** rather than creating a new one. It lets you change the message and/or add staged changes. The result **replaces** the last commit with a new commit object and a new hash.

    ```bash
    git add forgotten-file.js
    git commit --amend --no-edit   # add the file to the last commit, keep the message
    ```

    ⚠️ Avoid amending commits that have already been pushed to shared branches — it rewrites history.

    **[⬆ Back to Top](#table-of-contents)**

31. ### How do you modify the last commit message?

    Use `git commit --amend -m "New message"`:

    ```bash
    git commit --amend -m "Fix: correct typo in error message"
    # Or omit -m to edit interactively in your default editor:
    git commit --amend
    ```

    Ensure the commit hasn't been pushed to a branch others use, since amending rewrites the commit.

    **[⬆ Back to Top](#table-of-contents)**

32. ### What happens if you commit without staging files?

    If you run `git commit` with **nothing staged**, Git aborts and reports `nothing to commit, working tree clean` (or lists unstaged changes). The shortcut `git commit -a` automatically stages **all tracked files** that changed before committing — but it skips **new (untracked)** files.

    ```bash
    git commit -a -m "Quick fix"   # stages & commits tracked changes only
    ```

    **[⬆ Back to Top](#table-of-contents)**

33. ### How do you commit only specific files?

    Stage just the files you want, then commit:

    ```bash
    git add src/auth.js src/session.js
    git commit -m "Implement session handling"

    # Or stage selected hunks interactively
    git add -p src/auth.js
    git commit -m "Add only the validation hunk"
    ```

    **[⬆ Back to Top](#table-of-contents)**

34. ### What are atomic commits?

    **Atomic commits** encapsulate a **single logical change**. They make history easier to understand, review, and selectively revert. Aim to group related modifications (one feature or one bug fix) into a single commit with a clear message — never bundle unrelated changes together.

    **[⬆ Back to Top](#table-of-contents)**

35. ### Why should commits be small and meaningful?

    Small, well-named commits provide a **clear, navigable history**, making it easier to review changes, locate bugs (e.g., with `git bisect`), and revert specific features. Large commits that bundle unrelated changes are hard to understand and risky to revert. Use the staging area to curate exactly what each commit contains.

    **[⬆ Back to Top](#table-of-contents)**

36. ### What is a commit hash?

    A **commit hash** is the SHA-1 (or SHA-256) checksum that uniquely identifies a commit object — a 40-character hexadecimal string. Git uses it to refer to commits in branches, tags, and references. You can use a short, unambiguous prefix:

    ```bash
    git show a1b2c3d
    git revert a1b2c3d
    ```

    **[⬆ Back to Top](#table-of-contents)**

37. ### How do you view commit history?

    Use `git log` with helpful options:

    ```bash
    git log --oneline                          # one commit per line
    git log --graph --decorate --oneline --all # visualize branches & merges
    git log -p                                  # show the diff for each commit
    git log --author="Amandeep" --since="2 weeks ago"
    git log --stat                              # files changed per commit
    ```

    **[⬆ Back to Top](#table-of-contents)**

38. ### How do you view changes before committing?

    ```bash
    git diff            # working directory vs. index (unstaged changes)
    git diff --staged   # index vs. last commit (what WILL be committed)
    git status          # summary of staged & unstaged changes
    ```

    **[⬆ Back to Top](#table-of-contents)**

39. ### How do you compare staged and unstaged changes?

    Use `git diff` for **unstaged** changes and `git diff --staged` (alias `--cached`) for **staged** changes:

    ```bash
    git diff           # what you've changed but not yet staged
    git diff --staged  # what you've staged for the next commit
    git diff HEAD      # all changes since the last commit (staged + unstaged)
    ```

    **[⬆ Back to Top](#table-of-contents)**

40. ### How do you undo a staged file?

    Use `git restore --staged <file>` (modern) or `git reset <file>` (older) to unstage **without** altering your working directory:

    ```bash
    git restore --staged app.js   # unstage, keep working changes
    git reset app.js              # equivalent older syntax
    ```

    **[⬆ Back to Top](#table-of-contents)**


## Branching

41. ### What is a branch in Git?

    A **branch** is a lightweight, movable pointer to a commit. Creating a branch writes a small file under `.git/refs/heads/` containing a commit hash. Branches enable independent lines of development. Checking out a branch moves `HEAD` to it and updates your working directory.

    ```bash
    cat .git/refs/heads/main   # just a 40-char commit hash
    ```

    **[⬆ Back to Top](#table-of-contents)**

42. ### Why are branches used?

    Branches let you **isolate work** — features, experiments, bug fixes — so multiple developers can work concurrently without destabilizing the main codebase. When work is complete, you merge or rebase the branch back into another branch (e.g., `main`). Cheap branching is one of Git's defining strengths.

    **[⬆ Back to Top](#table-of-contents)**

43. ### How do you create a new branch?

    ```bash
    git branch feature/login          # create only (stay on current branch)
    git checkout -b feature/login     # create AND switch (classic)
    git switch -c feature/login       # create AND switch (Git ≥ 2.23)
    ```

    The new branch points to the current commit.

    **[⬆ Back to Top](#table-of-contents)**

44. ### How do you switch between branches?

    ```bash
    git checkout main      # classic
    git switch main        # modern (clearer intent)
    ```

    This moves `HEAD` to the target branch and updates the working directory. Git refuses to switch if it would overwrite uncommitted changes — stash or commit them first.

    **[⬆ Back to Top](#table-of-contents)**

45. ### What is the difference between git checkout and git switch?

    `git checkout` is a **versatile but overloaded** command — it switches branches, creates branches (`-b`), and restores files, which can be confusing. Since **Git 2.23**, two focused commands were introduced:

    - **`git switch`** — dedicated to switching/creating branches.
    - **`git restore`** — dedicated to restoring files.

    They perform similar underlying operations but make intent clearer and reduce mistakes.

    **[⬆ Back to Top](#table-of-contents)**

46. ### How do you create and switch to a branch in one command?

    ```bash
    git checkout -b new-feature    # classic
    git switch -c new-feature      # modern
    ```

    Both create the branch and immediately check it out.

    **[⬆ Back to Top](#table-of-contents)**

47. ### What is the HEAD pointer in Git?

    `HEAD` is a **symbolic reference to your current branch** (and thus the current commit). It normally points to a branch name, which in turn points to the latest commit on that branch. When you check out another branch, `HEAD` moves to point to it. In a **detached HEAD** state, `HEAD` points directly to a commit instead of a branch.

    ```bash
    cat .git/HEAD
    # ref: refs/heads/main   ← normal
    # <commit-hash>          ← detached
    ```

    **[⬆ Back to Top](#table-of-contents)**

48. ### What happens when you create a branch?

    Git writes a new reference under `.git/refs/heads/<branch-name>` pointing to the current commit. **No files are copied** — a branch is just a 40-byte pointer. This is why creating branches is instantaneous and inexpensive, even in huge repositories.

    **[⬆ Back to Top](#table-of-contents)**

49. ### How do you rename a branch?

    ```bash
    git branch -m new-name                 # rename the current branch
    git branch -m old-name new-name        # rename a specific branch

    # If already pushed, update the remote too:
    git push origin :old-name new-name     # delete old remote, push new
    git push --set-upstream origin new-name
    ```

    **[⬆ Back to Top](#table-of-contents)**

50. ### How do you delete a branch?

    ```bash
    git branch -d feature/login        # delete if fully merged (safe)
    git branch -D feature/login        # force delete (unmerged work lost)

    git push origin --delete feature/login   # delete the remote branch
    git push origin :feature/login           # older equivalent syntax
    ```

    **[⬆ Back to Top](#table-of-contents)**

51. ### What is a detached HEAD state?

    A **detached HEAD** occurs when you check out a specific commit (e.g., `git checkout abc1234`) or a tag instead of a branch. `HEAD` points directly to that commit. You can inspect and even commit there, but **new commits aren't attached to any branch** — and can become unreachable if you switch away without saving them.

    ```bash
    git checkout abc1234
    # You are in 'detached HEAD' state...
    ```

    **[⬆ Back to Top](#table-of-contents)**

52. ### How do you recover from a detached HEAD state?

    If you made commits in a detached HEAD and want to keep them, **create a branch** before switching away:

    ```bash
    git switch -c saved-work       # attach your detached commits to a branch
    # or
    git checkout -b saved-work
    ```

    If you already switched away, find the lost commit hash with `git reflog` and branch/cherry-pick from it.

    **[⬆ Back to Top](#table-of-contents)**

53. ### What are long-lived branches?

    **Long-lived branches** persist for the life of the project. Common examples include `main` (or `master`), `develop`, and `release` branches. They typically represent production code and active development streams, and changes flow into them through merges or rebases from shorter-lived branches.

    **[⬆ Back to Top](#table-of-contents)**

54. ### What are short-lived feature branches?

    **Short-lived branches** are created for a specific feature or bug fix and exist only for the duration of that task. They are merged back when complete and then deleted. Keeping them short-lived encourages clean histories, smaller diffs, and easier code review.

    **[⬆ Back to Top](#table-of-contents)**

55. ### What are branch naming conventions?

    Teams adopt naming conventions so collaborators can identify a branch's purpose at a glance:

    | Type | Example |
    | --- | --- |
    | Feature | `feature/login-form`, `feat/oauth` |
    | Bug fix | `bugfix/issue-123`, `fix/null-pointer` |
    | Release | `release/1.2.0` |
    | Hotfix | `hotfix/critical-payment-bug` |

    Many teams also embed an issue tracker ID (e.g., `feature/JIRA-456-add-search`).

    **[⬆ Back to Top](#table-of-contents)**


## Merging

56. ### What is Git merge?

    `git merge` **integrates changes from one branch into another**. Git finds the **merge base** (common ancestor) of the two branches and combines their changes into a new snapshot. If the histories diverged, Git creates a new **merge commit**; if not, it can fast-forward.

    ```bash
    git checkout main
    git merge feature/login
    ```

    **[⬆ Back to Top](#table-of-contents)**

57. ### What are the different types of merges?

    - **Fast-forward merge** — when the current branch hasn't diverged, Git simply moves the branch pointer forward; no merge commit is created.
    - **Three-way merge** — when branches have diverged, Git creates a new merge commit with two parents, combining both histories.
    - **Octopus merge** — merges more than two branches into a single commit at once.

    **[⬆ Back to Top](#table-of-contents)**

58. ### What is a fast-forward merge?

    A **fast-forward merge** occurs when there are **no divergent commits** — the target branch simply moves forward to the source branch's tip, producing a **linear history** with no merge commit.

    ```bash
    git checkout main
    git merge feature        # if main hasn't moved, this just fast-forwards

    git merge --no-ff feature  # force a merge commit even when FF is possible
    ```

    **[⬆ Back to Top](#table-of-contents)**

59. ### What is a three-way merge?

    A **three-way merge** is used when branches diverge. Git computes the **merge base** and diffs it against each branch tip, then applies both sets of changes, producing a new commit with **two parents**. Conflicts arise if both branches changed the same lines.

    ```
          A---B---C  feature
         /         \
    D---E-----------M   main (M is the merge commit)
    ```

    **[⬆ Back to Top](#table-of-contents)**

60. ### What is a merge commit?

    A **merge commit** is a commit with **multiple parent pointers**, representing the result of combining two or more histories. Its message typically records which branches were merged. Merge commits preserve the full branching topology in history.

    **[⬆ Back to Top](#table-of-contents)**

61. ### How do you merge one branch into another?

    ```bash
    git checkout main            # check out the target branch
    git merge feature/login      # merge the source branch in
    # If conflicts occur:
    #   1. edit the conflicted files
    git add resolved-file.js     #   2. stage resolutions
    git commit                   #   3. complete the merge (if not auto-committed)
    ```

    Use `--no-ff` to always create a merge commit and preserve the feature branch's existence in history.

    **[⬆ Back to Top](#table-of-contents)**

62. ### What is a merge conflict?

    A **merge conflict** happens when Git **cannot automatically reconcile** differences — e.g., two branches edit the same lines of a file differently, or one branch deletes a file another modifies. Git marks the conflicting sections and pauses, requiring you to resolve them manually.

    ```
    <<<<<<< HEAD
    const timeout = 30;
    =======
    const timeout = 60;
    >>>>>>> feature/login
    ```

    **[⬆ Back to Top](#table-of-contents)**

63. ### Why do merge conflicts occur?

    Conflicts occur when changes are **incompatible** between branches — typically when multiple developers modify the **same parts of a file**, or when file deletion/renaming collides with edits. Frequent integration (pulling/pushing often) and isolating features into separate areas of the code reduce conflict frequency.

    **[⬆ Back to Top](#table-of-contents)**

64. ### How do you resolve merge conflicts?

    1. **Identify conflicts** — Git marks them with `<<<<<<<`, `=======`, `>>>>>>>` and lists them in `git status`.
    2. **Edit files** — decide which changes to keep, possibly combining both sides, and remove the conflict markers.
    3. **Stage resolved files** — `git add <file>`.
    4. **Complete the merge** — `git commit`.
    5. **Test and verify** — make sure the project still builds and tests pass.

    ```bash
    git status              # see conflicted files
    # ...edit files to resolve...
    git add resolved.js
    git commit              # finalize the merge
    ```

    **[⬆ Back to Top](#table-of-contents)**

65. ### What tools can be used to resolve merge conflicts?

    - **`git mergetool`** with engines like vimdiff, Meld, or KDiff3.
    - **IDE tools** — Visual Studio Code's merge editor, IntelliJ, Eclipse.
    - **Web-based editors** — GitHub's and GitLab's in-browser conflict resolvers.

    ```bash
    git mergetool   # launches your configured visual merge tool
    ```

    **[⬆ Back to Top](#table-of-contents)**

66. ### How do you abort a merge operation?

    If a merge goes wrong before you commit the resolution, return to the pre-merge state:

    ```bash
    git merge --abort               # cleanly undo the in-progress merge
    git reset --merge               # alternative
    git reset --hard <commit>       # last resort: reset to a known-good commit
    ```

    **[⬆ Back to Top](#table-of-contents)**

67. ### How do you view merge history?

    ```bash
    git log --graph --oneline --decorate --all
    git log --merges          # show only merge commits
    gitk                      # GUI history viewer
    ```

    The graph reveals where branches diverged and merged.

    **[⬆ Back to Top](#table-of-contents)**

68. ### What are merge strategies in Git?

    Git supports several strategies via `git merge --strategy=<strategy>` (or `-s`):

    | Strategy | Behavior |
    | --- | --- |
    | `ort` (default, modern) | Optimized recursive three-way merge with rename handling |
    | `recursive` | Older default three-way merge |
    | `resolve` | Simpler two-parent algorithm |
    | `octopus` | Merges more than two branches |
    | `ours` | Keeps your branch's content, ignoring the other branch |
    | `subtree` | Merges a project added as a subtree |

    ```bash
    git merge -s ours legacy-branch   # record a merge but keep our content
    ```

    **[⬆ Back to Top](#table-of-contents)**

69. ### What is an octopus merge?

    An **octopus merge** merges **three or more branches simultaneously** into one commit. It's useful for combining many independent topic branches at once. However, if any branch conflicts, the octopus merge fails and you must merge the conflicting branches individually.

    ```bash
    git merge feature-a feature-b feature-c
    ```

    **[⬆ Back to Top](#table-of-contents)**

70. ### What are the disadvantages of frequent merging?

    - **Complex history** — many merge commits clutter the log and obscure a linear narrative.
    - **Harder conflicts** — branches that diverge for a long time before merging produce gnarly conflicts.
    - **Integration cost** — each merge may require coordination and re-running tests.

    Frequent **small** merges are far less disruptive than infrequent **large** ones, but still demand attention.

    **[⬆ Back to Top](#table-of-contents)**


## Rebasing

71. ### What is Git rebase?

    `git rebase` is an alternative to merge for integrating changes. It **reapplies (replays) a series of commits onto a new base commit**, creating **new commit hashes**. The result is a **linear history** with no merge commit.

    ```bash
    git checkout feature
    git rebase main     # replay feature's commits on top of the latest main
    ```

    **[⬆ Back to Top](#table-of-contents)**

72. ### How is rebase different from merge?

    - **Merge** preserves the branch structure and creates a merge commit with two parents (non-linear history).
    - **Rebase** rewrites history by replaying commits, producing a **straight line**.

    Both produce the **same final file snapshot**; only the history shape differs. Merge is non-destructive; rebase rewrites commits (new hashes).

    ```
    Merge:   A---B---C---M (main)        Rebase:  A---B---C---D'---E' (main)
                  \     /
                   D---E (feature)        feature replayed as D', E'
    ```

    **[⬆ Back to Top](#table-of-contents)**

73. ### When should you use rebase?

    Use rebase to maintain a **clean, linear history**, especially **before** pushing local work. Typical cases:

    - **Update a feature branch** — `git fetch origin && git rebase origin/main` to incorporate the latest upstream commits.
    - **Squash small commits** — via interactive rebase, combine WIP commits into one.

    ⚠️ **Avoid rebasing commits already pushed to shared branches** — it changes hashes and forces collaborators to reconcile diverged histories.

    **[⬆ Back to Top](#table-of-contents)**

74. ### What is interactive rebase?

    Interactive rebase (`git rebase -i <base>`) lets you **edit, reorder, squash, or drop** commits before reapplying them. Git opens a todo list in your editor:

    ```
    pick   0123abc add user model
    reword 4567def fix typo in README
    squash 89ab123 add API endpoint
    drop   cdef456 debugging leftovers
    ```

    Available actions: `pick`, `reword`, `edit`, `squash`, `fixup`, `drop`, and `exec`. Save to apply.

    **[⬆ Back to Top](#table-of-contents)**

75. ### How do you squash commits using rebase?

    Run interactive rebase over the range to squash. To combine the last three commits:

    ```bash
    git rebase -i HEAD~3
    ```

    In the todo list, keep `pick` on the first commit and change the rest to `squash` (keeps all messages) or `fixup` (discards their messages):

    ```
    pick   aaa111 implement search
    squash bbb222 fix search edge case
    fixup  ccc333 lint
    ```

    **[⬆ Back to Top](#table-of-contents)**

76. ### What is commit squashing?

    **Squashing** combines multiple commits into a single commit. It's commonly used to clean up a feature branch before merging, turning a series of WIP commits into one coherent change. Squashing doesn't change the final content — it rewrites history by producing new commit hashes.

    **[⬆ Back to Top](#table-of-contents)**

77. ### What are the benefits of rebasing?

    - **Linear history** — easier to read and follow with `git log`.
    - **Clean pull requests** — fewer merge commits; reviewers focus on your actual feature commits.
    - **Avoids redundant merges** — small feature branches can be replayed neatly onto `main`.

    **[⬆ Back to Top](#table-of-contents)**

78. ### What are the risks of rebasing shared branches?

    Rebasing **rewrites commit hashes**. If you rebase a branch others are using and force-push, their local histories diverge and they must reconcile (often via `git pull --rebase`), which is confusing and error-prone. The Pro Git guidance is clear: **never rebase commits that exist outside your repository and that others may have based work on.**

    **[⬆ Back to Top](#table-of-contents)**

79. ### How do you resolve conflicts during rebase?

    When a conflict arises, Git pauses the rebase:

    1. **Edit** the conflicting files to resolve them.
    2. **Stage** the resolved files: `git add <file>`.
    3. **Continue**: `git rebase --continue`.
    4. To **skip** the problematic commit: `git rebase --skip`.
    5. To **bail out** entirely: `git rebase --abort`.

    **[⬆ Back to Top](#table-of-contents)**

80. ### How do you continue a rebase after conflict resolution?

    After resolving conflicts and staging the files, run:

    ```bash
    git add resolved-file.js
    git rebase --continue
    ```

    Git applies the next commit in the series; repeat until all commits are reapplied.

    **[⬆ Back to Top](#table-of-contents)**

81. ### How do you abort a rebase?

    ```bash
    git rebase --abort
    ```

    This resets `HEAD` and the working directory back to the state **before** the rebase started — useful when conflicts become too complex or rebasing turns out to be the wrong choice.

    **[⬆ Back to Top](#table-of-contents)**

82. ### What is the difference between rebase and rebase --interactive?

    - **`git rebase`** simply replays your commits onto the new base, unchanged.
    - **`git rebase -i`** opens an interactive interface to **reorder, squash, edit, reword, or drop** commits before they're reapplied.

    Interactive rebase is the primary tool for **rewriting and curating commit history**.

    **[⬆ Back to Top](#table-of-contents)**

83. ### What is upstream in rebase?

    In the rebase context, **upstream** is the branch you're rebasing **onto**. In `git rebase origin/main`, you replay your current branch's commits on top of `origin/main`. "Upstream" can also refer more generally to the remote branch your local branch tracks (set via `git push --set-upstream`).

    **[⬆ Back to Top](#table-of-contents)**

84. ### How do you rebase a feature branch onto main?

    ```bash
    git fetch origin                # get the latest remote state
    git checkout feature
    git rebase origin/main          # replay feature on top of latest main
    # resolve any conflicts, then continue
    git push --force-with-lease     # if the branch was already pushed
    ```

    `--force-with-lease` updates the remote safely, refusing to overwrite others' new work.

    **[⬆ Back to Top](#table-of-contents)**

85. ### What are best practices for rebasing?

    - **Rebase only local/unpublished work** — never published commits on shared branches.
    - **Rebase before merging** — replay your feature onto `main` before opening a PR to minimize merge commits.
    - **Use interactive rebase** — squash and reword to produce a clean history.
    - **Use `--force-with-lease`** — when pushing after a rebase, to avoid clobbering teammates' work.

    **[⬆ Back to Top](#table-of-contents)**


## Undoing Changes

86. ### How do you undo uncommitted changes?

    It depends on whether changes are staged or unstaged:

    ```bash
    # Unstaged modifications — discard working-directory changes
    git restore <file>
    git restore .                       # all files

    # Staged changes — unstage but keep edits
    git restore --staged <file>

    # Discard BOTH staged and working changes for a file
    git restore --source=HEAD --staged --worktree <file>
    ```

    **[⬆ Back to Top](#table-of-contents)**

87. ### What is the difference between reset, revert and restore?

    | Command | What it does | History impact | Shared-branch safe? |
    | --- | --- | --- | --- |
    | **`reset`** | Moves `HEAD` (and optionally index/working dir) to a commit | Rewrites history | ❌ No |
    | **`revert`** | Creates a **new commit** that undoes a previous one | Preserves history | ✅ Yes |
    | **`restore`** | Restores file content in the working tree or index | No history change | ✅ Yes |

    Use **reset** for local cleanup, **revert** to safely undo on shared branches, and **restore** to recover individual files.

    **[⬆ Back to Top](#table-of-contents)**

88. ### What is git restore?

    `git restore` (Git ≥ 2.23) restores working-directory files or the staging area from a commit. It's a clearer alternative to the overloaded `git checkout`/`git reset`:

    ```bash
    git restore app.js                      # discard working-dir changes
    git restore --staged app.js             # unstage
    git restore --source=HEAD~2 app.js      # restore file from an older commit
    ```

    It **does not** modify commit history.

    **[⬆ Back to Top](#table-of-contents)**

89. ### What is git reset?

    `git reset` moves `HEAD` to a specified commit and optionally adjusts the index and working directory. It has three modes:

    - **`--soft`** — moves `HEAD` only; index and working dir are untouched (changes stay staged).
    - **`--mixed`** (default) — moves `HEAD` and resets the index; working dir untouched (changes become unstaged).
    - **`--hard`** — resets `HEAD`, index, **and** working dir; **all uncommitted changes are discarded**.

    ```bash
    git reset --soft  HEAD~1   # undo last commit, keep changes staged
    git reset --mixed HEAD~1   # undo last commit, unstage changes
    git reset --hard  HEAD~1   # undo last commit, discard changes (dangerous)
    ```

    **[⬆ Back to Top](#table-of-contents)**

90. ### What is the difference between soft, mixed and hard reset?

    | Mode | Resets HEAD | Resets Index | Resets Working Dir | Use case |
    | --- | --- | --- | --- | --- |
    | **soft** | ✔ | ✖ | ✖ | Re-commit with a new message; squash commits |
    | **mixed** | ✔ | ✔ | ✖ | Unstage changes but keep file edits |
    | **hard** | ✔ | ✔ | ✔ | Completely discard changes (⚠️ destructive) |

    **[⬆ Back to Top](#table-of-contents)**

91. ### When should you use a soft reset?

    Use a **soft reset** to undo the last commit(s) while **keeping the changes staged**. This is ideal for fixing a commit message or combining several commits into one:

    ```bash
    git reset --soft HEAD~1
    git commit -m "Better message"   # re-commit the same staged changes
    ```

    **[⬆ Back to Top](#table-of-contents)**

92. ### When should you use a hard reset?

    Use a **hard reset** to **discard all uncommitted changes** and return the working directory to a specific commit. A common use is aligning a local branch exactly with its remote:

    ```bash
    git reset --hard origin/main   # discard local changes, match remote
    ```

    ⚠️ This is irreversible for uncommitted work — use with caution.

    **[⬆ Back to Top](#table-of-contents)**

93. ### What is git revert?

    `git revert` creates a **new commit that reverses the changes** introduced by a specified commit. Because it adds a commit rather than rewriting history, it's the **safe way to undo on shared branches**.

    ```bash
    git revert a1b2c3d      # creates a new commit undoing a1b2c3d
    ```

    **[⬆ Back to Top](#table-of-contents)**

94. ### Why is revert preferred in shared repositories?

    Reverting **preserves history** and avoids rewriting commits others may have based work on. Using `git reset` or `git commit --amend` on a shared branch disrupts collaborators' histories, whereas `git revert` simply appends a new, reversing commit — keeping everyone's history consistent.

    **[⬆ Back to Top](#table-of-contents)**

95. ### How do you revert multiple commits?

    ```bash
    # Revert a contiguous range (the ^ includes the oldest commit)
    git revert <oldest>^..<newest>

    # Revert specific, unrelated commits
    git revert abc1234 def5678

    # Revert a range without committing each one individually
    git revert --no-commit <oldest>^..<newest>
    git commit -m "Revert problematic feature"
    ```

    **[⬆ Back to Top](#table-of-contents)**

96. ### How do you undo the last commit without losing changes?

    ```bash
    git reset --soft HEAD~1   # move HEAD back one commit, keep changes staged
    # then re-commit, or continue editing

    # On a shared branch, prefer:
    git revert HEAD           # new commit that reverses the last one
    ```

    **[⬆ Back to Top](#table-of-contents)**

97. ### How do you remove a file from a commit?

    To pull a file out of the **last** commit while keeping it on disk:

    ```bash
    git restore --staged secret.env   # unstage the file
    git rm --cached secret.env        # stop tracking, keep on disk
    git commit --amend                # rewrite the last commit without it
    ```

    For older commits, use interactive rebase (`git rebase -i`) to edit the relevant commit.

    **[⬆ Back to Top](#table-of-contents)**

98. ### How do you recover deleted commits?

    Git keeps a **reflog** of where `HEAD` and branches have pointed. Find the lost commit and restore it:

    ```bash
    git reflog                        # find the commit hash
    git checkout <hash>               # inspect it
    git reset --hard <hash>           # restore a branch to it
    git branch recovered <hash>       # or save it to a new branch
    ```

    Reflog entries typically expire after ~90 days.

    **[⬆ Back to Top](#table-of-contents)**

99. ### What is the Git reflog?

    The **reflog** (reference log) records updates to `HEAD` and branch tips locally. It lets you recover commits that are no longer referenced by any branch or tag — for example, after an accidental `git reset --hard` or a botched rebase.

    ```bash
    git reflog
    # a1b2c3d HEAD@{0}: reset: moving to HEAD~1
    # d4e5f6g HEAD@{1}: commit: add feature
    ```

    **[⬆ Back to Top](#table-of-contents)**

100. ### How does reflog help in recovery scenarios?

     When you rewrite history (rebase, reset, amend), the original commits become **unreachable** but remain in the reflog. Use `git reflog` to find their hashes, then create a branch or reset to recover them. Because reflogs are **local** and not shared, this safety net exists only on the machine where the action happened, and entries eventually expire.

     **[⬆ Back to Top](#table-of-contents)**


## Remote Repositories

101. ### What is a remote repository?

     A **remote** is a hosted version of your repository, typically on a server or service like GitHub or GitLab. Remotes enable collaboration: you push local commits and pull others' changes. They're configured with names (e.g., `origin`) and URLs.

     **[⬆ Back to Top](#table-of-contents)**

102. ### What is the difference between git fetch and git pull?

     - **`git fetch`** downloads objects and updates remote-tracking branches (e.g., `origin/main`) **without** touching your working branch. Safe to run anytime.
     - **`git pull`** runs `git fetch` **followed by a merge (or rebase)** into your current branch, immediately applying changes — which can produce conflicts if your branch diverged.

     ```bash
     git fetch origin              # review remote changes first
     git log HEAD..origin/main     # see what's new before integrating
     git pull origin main          # fetch + merge in one step
     git pull --rebase origin main # fetch + rebase (linear history)
     ```

     **[⬆ Back to Top](#table-of-contents)**

103. ### What does git fetch do?

     `git fetch` retrieves commit objects, tags, and updated branch references from the remote, storing them under `refs/remotes/<remote>/`. It **does not** modify your local branches or working directory — making it ideal for reviewing changes before integrating them.

     **[⬆ Back to Top](#table-of-contents)**

104. ### What does git pull do?

     `git pull` combines `git fetch` with `git merge` (or `git rebase`, if configured). After fetching, it integrates the remote-tracking branch into your current branch. Set rebase as the default with:

     ```bash
     git config --global pull.rebase true
     ```

     **[⬆ Back to Top](#table-of-contents)**

105. ### What is the difference between pull and merge?

     `git pull` is a **convenience command** that fetches **and then** merges (or rebases) remote changes into your current branch. `git merge` only combines two branches **already present locally**. Fetching first and merging manually gives you more control over what gets integrated and when.

     **[⬆ Back to Top](#table-of-contents)**

106. ### How do you push changes to a remote repository?

     ```bash
     git push origin main
     git push --set-upstream origin feature/login   # first push of a new branch
     git push -u origin feature/login               # shorthand for the above
     ```

     `--set-upstream` (`-u`) establishes a tracking relationship so future `git push`/`git pull` need no arguments.

     **[⬆ Back to Top](#table-of-contents)**

107. ### What is force push?

     `git push --force` bypasses the fast-forward safety check and **overwrites the remote branch** with your local branch. It's typically needed after rewriting history (e.g., a rebase), but it can **delete commits on the remote** that aren't in your local history — dangerous on shared branches.

     **[⬆ Back to Top](#table-of-contents)**

108. ### When is force push dangerous?

     Force pushing can **remove commits collaborators depend on**, causing lost work and confusing conflicts. Never force-push to shared branches like `main` or `develop`. When a force push is unavoidable (after a rebase of your own branch), prefer **`--force-with-lease`**, which refuses to overwrite if the remote moved since your last fetch.

     **[⬆ Back to Top](#table-of-contents)**

109. ### What is git push --force-with-lease?

     `git push --force-with-lease` behaves like a force push but adds a **safety check**: it verifies the remote branch pointer is exactly where you last saw it. If someone else pushed in the meantime, the push is **refused** — preventing you from accidentally overwriting their work.

     ```bash
     git push --force-with-lease origin feature/login
     ```

     **[⬆ Back to Top](#table-of-contents)**

110. ### What is upstream tracking?

     **Upstream tracking** associates a local branch with a remote branch. Once set, `git push` and `git pull` without arguments use that relationship. Configure it with:

     ```bash
     git push --set-upstream origin feature
     git branch --set-upstream-to=origin/feature
     ```

     **[⬆ Back to Top](#table-of-contents)**

111. ### How do you set an upstream branch?

     ```bash
     git push --set-upstream origin feature             # on first push
     git branch --set-upstream-to=origin/feature local-feature  # for an existing branch
     ```

     **[⬆ Back to Top](#table-of-contents)**

112. ### How do you view remote branches?

     ```bash
     git branch -r        # remote-tracking branches (e.g., origin/main)
     git branch -a        # all branches: local + remote
     git remote show origin   # detailed remote info
     ```

     **[⬆ Back to Top](#table-of-contents)**

113. ### How do you delete a remote branch?

     ```bash
     git push origin --delete feature/login   # modern
     git push origin :feature/login           # older syntax
     ```

     This removes the branch from the remote only; local branches are untouched. Confirm with your team before deleting shared branches.

     **[⬆ Back to Top](#table-of-contents)**

114. ### What are remote tracking branches?

     **Remote-tracking branches** (e.g., `origin/main`, `origin/feature`) are **read-only local references** reflecting the state of branches on the remote. They're updated by `git fetch`. You can't commit to them directly; instead, you merge or rebase them into your local branches.

     **[⬆ Back to Top](#table-of-contents)**

115. ### What happens when multiple developers push simultaneously?

     If two developers push to the same branch, the second push is **rejected** if it wouldn't be a fast-forward. The second developer must **pull** (merge or rebase) the new remote commits, resolve any conflicts, and push again. Using feature branches and pulling frequently prevents most such collisions. Force-pushing in this situation risks overwriting the other developer's work.

     **[⬆ Back to Top](#table-of-contents)**


## Stashing

116. ### What is Git stash?

     `git stash` temporarily **shelves uncommitted changes** (modified tracked files and staged changes) onto a stack, leaving your working directory clean. You can then switch branches or pull updates and reapply the changes later.

     ```bash
     git stash            # shelve current changes
     git stash list       # view the stash stack
     ```

     **[⬆ Back to Top](#table-of-contents)**

117. ### When should you use stash?

     Use stashing to **temporarily save unfinished work** without committing it. Common scenarios:

     - You need to **switch branches** to fix an urgent bug.
     - You want to **pull** updates but have local changes that would conflict.

     Stashing lets you set work aside cleanly and restore it afterward.

     **[⬆ Back to Top](#table-of-contents)**

118. ### How do you create a stash?

     ```bash
     git stash                       # or: git stash push
     git stash push -m "WIP: login form"   # with a descriptive message
     ```

     Git saves the index and working-directory state, clears your changes, and records the stash under `refs/stash`.

     **[⬆ Back to Top](#table-of-contents)**

119. ### How do you list available stashes?

     ```bash
     git stash list
     # stash@{0}: WIP on main: 049d078 Create index file
     # stash@{1}: On feature: experiment
     ```

     Stashes are listed LIFO (most recent first), each showing the branch and commit you were on.

     **[⬆ Back to Top](#table-of-contents)**

120. ### How do you apply a stash?

     ```bash
     git stash apply              # reapply the most recent stash (keeps it on the stack)
     git stash apply stash@{2}    # reapply a specific stash
     git stash apply --index      # also restore the staged state
     ```

     **[⬆ Back to Top](#table-of-contents)**

121. ### What is the difference between git stash apply and git stash pop?

     - **`git stash apply`** reapplies the stash but **keeps it** on the stack (you can apply it again).
     - **`git stash pop`** reapplies the stash **and removes it** from the stack.

     ```bash
     git stash pop          # apply + drop the latest stash
     git stash apply        # apply but retain
     ```

     If conflicts occur during `pop`, the stash may still be dropped — recover it via the reflog if needed.

     **[⬆ Back to Top](#table-of-contents)**

122. ### How do you delete a stash?

     ```bash
     git stash drop stash@{0}   # remove a specific stash
     git stash clear            # remove ALL stashes (irreversible)
     ```

     Be careful — dropped stashes are hard to recover (only via dangling-commit lookup).

     **[⬆ Back to Top](#table-of-contents)**

123. ### Can untracked files be stashed?

     By default, `git stash` only stores **tracked** file changes. To include untracked files, add `-u`; to also include ignored files, use `-a`:

     ```bash
     git stash push -u    # include untracked files
     git stash push -a    # include untracked AND ignored files
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Tags and Releases

124. ### What is a tag in Git?

     A **tag** is a named reference to a specific commit, typically used to mark release points (e.g., `v1.0.0`). Unlike branches, **tags don't move** — they permanently point to the same commit. Tags can be lightweight or annotated.

     **[⬆ Back to Top](#table-of-contents)**

125. ### What is the difference between lightweight and annotated tags?

     - **Lightweight tags** — simple pointers to a commit, storing only the hash. Like a bookmark, with no extra metadata.
     - **Annotated tags** — full objects in Git's database, storing the tagger's name, email, date, and a message; they can be GPG-signed.

     **Annotated tags are recommended for releases** because they carry metadata and can be verified.

     ```bash
     git tag v1.0.0                              # lightweight
     git tag -a v1.0.0 -m "Release 1.0.0"        # annotated
     ```

     **[⬆ Back to Top](#table-of-contents)**

126. ### How do you create a tag?

     ```bash
     git tag v1.0.0                                  # lightweight at HEAD
     git tag -a v1.0.0 -m "Release version 1.0.0"    # annotated
     git tag -a v1.0.0 9fceb02 -m "Release"          # tag a specific commit
     git tag -s v1.0.0 -m "Signed release"           # GPG-signed
     ```

     **[⬆ Back to Top](#table-of-contents)**

127. ### How do you push tags to a remote repository?

     ```bash
     git push origin v1.0.0     # push a single tag
     git push origin --tags     # push all tags
     git push --follow-tags     # push commits + annotated tags they reference
     ```

     Tags are **not** pushed automatically with `git push` — you must push them explicitly.

     **[⬆ Back to Top](#table-of-contents)**

128. ### How do you delete a tag?

     ```bash
     git tag -d v1.0.0                    # delete locally
     git push origin --delete v1.0.0      # delete on the remote
     ```

     Be cautious deleting tags tied to releases or dependencies.

     **[⬆ Back to Top](#table-of-contents)**

129. ### Why are tags important in release management?

     Tags mark **immutable points** in history. Release pipelines use them to identify the exact codebase snapshot to build and deploy. **Semantic version tags** (`vMAJOR.MINOR.PATCH`) communicate compatibility, and tags let users check out a precise version for debugging or reproduction.

     **[⬆ Back to Top](#table-of-contents)**

130. ### How do teams use tags in CI/CD pipelines?

     Teams often **trigger pipelines on tags**. For example, pushing an annotated tag `v1.2.0` can trigger a build, run tests, and deploy to production. Because a tag pins an exact commit, builds are **reproducible** and traceable to a known state.

     ```yaml
     # Example GitHub Actions trigger
     on:
       push:
         tags:
           - 'v*.*.*'
     ```

     **[⬆ Back to Top](#table-of-contents)**


## Git Internals

131. ### How does Git store objects internally?

     Git uses four object types, all stored under `.git/objects/` and identified by hash:

     | Object | Stores |
     | --- | --- |
     | **Blob** | File content (no name or metadata) |
     | **Tree** | A directory listing: names, modes, and pointers to blobs/trees |
     | **Commit** | A snapshot: root tree, parent(s), author/committer, message |
     | **Tag** | An annotated tag: target object + tagger metadata |

     Git compresses and groups objects into **packfiles** for efficiency.

     **[⬆ Back to Top](#table-of-contents)**

132. ### What are blob objects in Git?

     **Blobs** store the **contents of a file** — nothing else. They contain no file name or metadata beyond the file mode. Because blobs are content-addressed by hash, two identical files share a single blob (**deduplication**); trees supply the names that reference blobs.

     **[⬆ Back to Top](#table-of-contents)**

133. ### What are tree objects in Git?

     **Tree objects** represent **directories**. A tree lists entries for files and subdirectories with their modes and object hashes. A commit references a single top-level tree, which recursively defines the entire repository state at that commit.

     ```bash
     git cat-file -p HEAD^{tree}
     # 100644 blob a1b2c3...  README.md
     # 040000 tree d4e5f6...  src
     ```

     **[⬆ Back to Top](#table-of-contents)**

134. ### What are commit objects in Git?

     A **commit object** records a snapshot and stores:

     - The **tree hash** (root directory snapshot).
     - **Parent commit hash(es)** — one for a normal commit, multiple for a merge.
     - **Author and committer** info (name, email, timestamps).
     - The **commit message**.

     **[⬆ Back to Top](#table-of-contents)**

135. ### What are tag objects in Git?

     A **tag object** references another object (usually a commit) and stores metadata: the tagger's name, email, date, and message. **Annotated tags** are implemented as tag objects, while **lightweight tags** are just refs under `refs/tags/` pointing directly at a commit.

     **[⬆ Back to Top](#table-of-contents)**

136. ### What is the Git object database?

     The **object database** lives in `.git/objects/` and holds every object (blobs, trees, commits, annotated tags) keyed by hash. Git compresses and packs objects into **packfiles** for efficiency. Because access is content-addressed and local, lookups are extremely fast.

     **[⬆ Back to Top](#table-of-contents)**

137. ### What is packfile compression?

     As objects accumulate, Git compresses them into **packfiles** — via `git gc` (garbage collect) or automatically during network transfer. Packfiles store many objects together using **delta compression** between similar objects, dramatically reducing disk usage and speeding up clone/fetch.

     ```bash
     git gc                    # compress loose objects into packfiles
     git count-objects -vH     # see loose vs. packed object stats
     ```

     **[⬆ Back to Top](#table-of-contents)**

138. ### How does Git achieve high performance?

     - **Local operations** — most commands run on the local clone, with no network latency.
     - **Efficient data structures** — snapshot storage, hashing, and packfiles make reads/writes fast.
     - **Cheap branches and merges** — branches are just pointers; merges use efficient algorithms.
     - **Caching** — Git caches filesystem state (via the index) to detect changes quickly.

     **[⬆ Back to Top](#table-of-contents)**


## Git Workflows & Best Practices

139. ### What is Git Flow?

     **Git Flow** is a structured branching model with defined roles:

     - **`main`** — production code.
     - **`develop`** — ongoing integration.
     - **Feature branches** — off `develop` for new features.
     - **Release branches** — off `develop` to stabilize a release; merge into both `main` and `develop`.
     - **Hotfix branches** — off `main` to fix critical issues; merge into both `main` and `develop`.

     It provides structure for larger projects with scheduled releases but can be heavyweight for continuous deployment.

     **[⬆ Back to Top](#table-of-contents)**

140. ### What is GitHub Flow?

     **GitHub Flow** is a lightweight workflow:

     - A single long-lived branch (`main`).
     - Short-lived **feature branches** named after the task or issue.
     - **Pull requests** for code review before merging.
     - **Continuous deployment** triggered by merging to `main`.

     It emphasizes rapid, frequent releases and suits web apps that deploy continuously.

     **[⬆ Back to Top](#table-of-contents)**

141. ### What is GitLab Flow?

     **GitLab Flow** combines feature branching with **environment branches** (e.g., `pre-prod`, `production`) that mirror your deployment pipeline. It adapts release handling to whether your project is version-based or environment-based and integrates issue tracking and CI/CD — bridging the gap between Git Flow's structure and GitHub Flow's simplicity.

     **[⬆ Back to Top](#table-of-contents)**

142. ### What is Trunk-Based Development?

     In **Trunk-Based Development**, developers integrate into a single shared branch (the "trunk" or `main`) very frequently. **Feature flags**, branch-by-abstraction, and incremental commits enable continuous integration. Any feature branches are extremely short-lived (often merged within a day). This minimizes merge conflicts and supports continuous delivery — popular at scale (e.g., Google).

     **[⬆ Back to Top](#table-of-contents)**

143. ### Which Git workflow is most suitable for Agile teams?

     It depends on team size and release cadence. Many Agile teams prefer **GitHub Flow** or **Trunk-Based Development** because they encourage frequent integration and small increments. **Git Flow** adds overhead when releases are frequent, but suits projects with scheduled, versioned releases. Choose the workflow that matches your deployment strategy.

     **[⬆ Back to Top](#table-of-contents)**

144. ### How do you handle hotfixes in Git?

     Create a branch off the production branch (e.g., `main`), fix and test the issue, then merge it back into **both** `main` and `develop` (or your active development branch). Tag the fix if it corresponds to a release, and communicate with the team so everyone incorporates it.

     ```bash
     git checkout -b hotfix/critical-bug main
     # ...fix & test...
     git checkout main && git merge hotfix/critical-bug
     git tag -a v1.2.1 -m "Hotfix"
     git checkout develop && git merge hotfix/critical-bug
     ```

     **[⬆ Back to Top](#table-of-contents)**

145. ### What branching strategy do you follow in your current project?

     *(This answer varies by project.)* A strong response describes your team's chosen workflow and **why** it fits — for example: "We use trunk-based development with short-lived feature branches and feature flags, PR review required, and CI running on every push. Releases are cut by tagging `main`, which triggers our deploy pipeline." Mention conventions for branch names, PRs, and code review.

     **[⬆ Back to Top](#table-of-contents)**

146. ### How do you review code using pull requests?

     1. Ensure the branch is **up to date** with `main` (rebase or merge).
     2. **Open a PR** on your hosting platform.
     3. **Reviewers** examine commits, discuss changes, and request adjustments.
     4. **Address comments** — push new commits and resolve conversations.
     5. Once **approved and tests pass**, merge into the target branch.

     **[⬆ Back to Top](#table-of-contents)**

147. ### What Git best practices do you follow in large teams?

     - **Write clear commit messages** — a concise summary line plus a body explaining the "why".
     - **Use feature branches** — isolate work and keep `main` stable.
     - **Rebase before merging** — maintain a linear history where appropriate.
     - **Avoid force pushes on shared branches** — use `--force-with-lease` and coordinate.
     - **Review and test** — PRs, automated tests, and CI pipelines.
     - **Use `.gitignore`** — keep build artifacts, secrets, and local config out of the repo.
     - **Tag releases** — mark milestones and maintain release notes.

     **[⬆ Back to Top](#table-of-contents)**

148. ### How do you maintain a clean commit history?

     - **Small, atomic commits** — one logical change each.
     - **Descriptive messages** — explain the "why", not just the "what".
     - **Interactive rebase** — squash and reorder before merging.
     - **Avoid committing generated files** — use `.gitignore`.
     - **Delete obsolete branches** — remove merged branches locally and remotely.

     **[⬆ Back to Top](#table-of-contents)**

149. ### How do you handle release branches in production systems?

     Release branches allow final bug fixing and stabilization:

     1. **Create** a release branch from `develop` (Git Flow) or `main`.
     2. **Freeze features** — only bug fixes and release-specific changes allowed.
     3. **Tag** the release (e.g., `v1.2.0`) when ready.
     4. **Merge** the release branch back into `main` (and `develop` if using Git Flow), then delete it.

     **[⬆ Back to Top](#table-of-contents)**

150. ### What are the most common Git mistakes and how can they be avoided?

     | Mistake | How to avoid |
     | --- | --- |
     | **Forgetting to pull before pushing** | Always `fetch`/`pull` first to avoid rejected pushes |
     | **Committing secrets or build artifacts** | Use `.gitignore` and secret scanning |
     | **Large commits with unrelated changes** | Break into small commits; use the staging area |
     | **Rebasing published history** | Use `revert`/`merge` on shared branches instead |
     | **Force pushing without care** | Prefer `--force-with-lease`; communicate with the team |
     | **Ignoring merge conflicts** | Take time to understand and resolve them properly |
     | **Not using branches** | Always work on feature branches to keep `main` stable |

     **[⬆ Back to Top](#table-of-contents)**


## Advanced & Scenario-Based Questions

151. ### What is git cherry-pick and when do you use it?

     `git cherry-pick` applies the changes from **specific commits** onto your current branch, creating new commits with new hashes. It's useful for **backporting a bug fix** to a release branch without merging an entire feature branch.

     ```bash
     git checkout release/1.2
     git cherry-pick a1b2c3d            # apply one commit
     git cherry-pick a1b2c3d..f6g7h8i   # apply a range
     git cherry-pick -n a1b2c3d         # apply without committing (stage only)
     ```

     ⚠️ Cherry-picking duplicates commits, so avoid it where a proper merge would be cleaner.

     **[⬆ Back to Top](#table-of-contents)**

152. ### What is the difference between git reset and git checkout for files?

     Both can restore file content, but they differ subtly:

     - **`git checkout -- <file>`** (or `git restore <file>`) overwrites the **working-directory** file with the version from the index (or a commit).
     - **`git reset <file>`** (mixed) **unstages** the file — it changes the index to match HEAD but **leaves the working directory alone**.

     In short: `reset` operates on the **index**; `checkout`/`restore` operates on the **working tree**. Modern Git splits these into `git restore` and `git restore --staged` for clarity.

     **[⬆ Back to Top](#table-of-contents)**

153. ### What is git bisect and how does it help debug?

     `git bisect` performs a **binary search through commit history** to find the commit that introduced a bug. You mark a known-good and known-bad commit; Git checks out the midpoint, you test, and mark it good or bad — halving the search space each time.

     ```bash
     git bisect start
     git bisect bad                 # current commit is broken
     git bisect good v1.0.0         # this old version worked
     # Git checks out a midpoint commit — test it, then:
     git bisect good   # or: git bisect bad
     # ...repeat until Git identifies the culprit...
     git bisect reset               # return to the original HEAD
     ```

     You can even automate it: `git bisect run ./test.sh`.

     **[⬆ Back to Top](#table-of-contents)**

154. ### What are Git hooks?

     **Git hooks** are scripts in `.git/hooks/` that run automatically at certain points in the Git lifecycle. They enable automation and policy enforcement.

     | Hook | Fires |
     | --- | --- |
     | `pre-commit` | Before a commit is created (e.g., run linters/tests) |
     | `commit-msg` | To validate the commit message format |
     | `pre-push` | Before pushing (e.g., run the test suite) |
     | `post-merge` | After a merge completes |
     | `pre-receive` / `update` | Server-side, to enforce policies on push |

     Tools like **Husky** (JS) or **pre-commit** (Python) manage shareable hooks across a team, since `.git/hooks` isn't committed by default.

     **[⬆ Back to Top](#table-of-contents)**

155. ### What is the difference between a fork and a clone?

     - A **clone** is a local copy of a repository on your machine, linked to the original via `origin`.
     - A **fork** is a **server-side copy** under your own account (a GitHub/GitLab concept, not native Git). You typically fork a project you don't have write access to, clone your fork, then open pull requests back to the original ("upstream").

     ```bash
     # Common fork workflow
     git clone https://github.com/you/forked-repo.git
     git remote add upstream https://github.com/original/repo.git
     git fetch upstream
     git rebase upstream/main
     ```

     **[⬆ Back to Top](#table-of-contents)**

156. ### What are Git submodules?

     **Submodules** let you embed one Git repository inside another at a specific commit — useful for shared libraries you want to version independently.

     ```bash
     git submodule add https://github.com/user/lib.git libs/lib
     git submodule update --init --recursive   # after cloning a repo with submodules
     git clone --recurse-submodules <url>      # clone everything in one step
     ```

     Submodules pin an exact commit of the dependency, but add workflow complexity — alternatives include subtrees and package managers.

     **[⬆ Back to Top](#table-of-contents)**

157. ### What is git worktree?

     `git worktree` lets you check out **multiple branches simultaneously** in separate directories backed by the same repository — no second clone needed. Great for fixing an urgent bug while keeping a feature branch checked out elsewhere.

     ```bash
     git worktree add ../hotfix-dir hotfix/urgent   # new working tree on a branch
     git worktree list
     git worktree remove ../hotfix-dir
     ```

     **[⬆ Back to Top](#table-of-contents)**

158. ### What is the difference between git merge --squash and interactive squash?

     - **`git merge --squash <branch>`** takes all the changes from a branch and stages them as a **single uncommitted change set** on the current branch — you then make one commit. The source branch's individual commits are **not** recorded as parents.
     - **Interactive squash** (`git rebase -i`) combines commits **within a branch** into fewer commits, rewriting that branch's own history.

     Use `--squash` to collapse a whole feature into one commit on `main`; use interactive rebase to tidy a branch's internal history before review.

     ```bash
     git checkout main
     git merge --squash feature/login
     git commit -m "Add login feature"   # single squashed commit
     ```

     **[⬆ Back to Top](#table-of-contents)**

159. ### How do you find who changed a line of code?

     Use `git blame` to see the commit, author, and timestamp for each line of a file:

     ```bash
     git blame app.js
     git blame -L 40,60 app.js          # only lines 40–60
     git log -S "functionName" --oneline  # find commits that added/removed a string
     git log -p -- app.js               # full change history of a file
     ```

     `git blame` answers "who and when"; `git log -S` (the "pickaxe") finds where a piece of code was introduced or removed.

     **[⬆ Back to Top](#table-of-contents)**

160. ### How would you remove sensitive data committed to a repository?

     Removing a secret from the latest commit is easy; removing it from **all history** requires rewriting:

     ```bash
     # Recommended modern tool: git-filter-repo
     git filter-repo --path secrets.env --invert-paths

     # Or the BFG Repo-Cleaner
     bfg --delete-files secrets.env
     ```

     After rewriting, **force-push** and have collaborators re-clone. Crucially, **rotate the leaked credentials** — once pushed, assume they're compromised regardless of history rewriting.

     **[⬆ Back to Top](#table-of-contents)**

161. ### What is a shallow clone and when is it useful?

     A **shallow clone** downloads only recent history (limited commit depth), saving time and disk space — ideal for **CI/CD pipelines** that only need the latest code.

     ```bash
     git clone --depth 1 https://github.com/user/repo.git   # only the latest commit
     git fetch --unshallow                                  # later, get full history
     ```

     The trade-off: limited history means commands like `git log` and `git blame` see only the fetched depth.

     **[⬆ Back to Top](#table-of-contents)**

162. ### How do you handle a large binary file in Git?

     Git is optimized for text, not large binaries, which bloat history. Use **Git LFS (Large File Storage)**, which stores large files outside the main repo and keeps lightweight pointers in Git:

     ```bash
     git lfs install
     git lfs track "*.psd"        # track Photoshop files via LFS
     git add .gitattributes
     git add design.psd
     git commit -m "Add design via LFS"
     ```

     For files accidentally committed before, rewrite history with `git filter-repo` and migrate them to LFS.

     **[⬆ Back to Top](#table-of-contents)**

163. ### What is the difference between HEAD, working tree, and index?

     These are Git's three "trees":

     | Concept | What it represents |
     | --- | --- |
     | **HEAD** | The last commit on the current branch — the snapshot you're based on |
     | **Index (staging area)** | The proposed next commit — what `git add` populates |
     | **Working tree** | The actual files on disk you're editing |

     `git status` essentially compares these three. `git diff` shows working-tree vs. index; `git diff --staged` shows index vs. HEAD.

     **[⬆ Back to Top](#table-of-contents)**

164. ### How do you resolve "your branch has diverged" errors?

     This happens when your local branch and its remote both have commits the other lacks. Decide how to integrate:

     ```bash
     git fetch origin

     # Option A — rebase your work on top of remote (linear history)
     git pull --rebase origin main

     # Option B — merge remote into yours (creates a merge commit)
     git pull origin main

     # If you intentionally want to discard local divergence:
     git reset --hard origin/main   # ⚠️ destroys local commits
     ```

     Choose rebase for a clean history on your own branch; choose merge when the divergence reflects legitimate parallel work.

     **[⬆ Back to Top](#table-of-contents)**

165. ### How would you undo a pushed commit on a shared branch?

     Since others may have pulled the commit, **never rewrite shared history**. Use `git revert` to add a new commit that reverses it:

     ```bash
     git revert <commit-hash>   # safe: creates a reversing commit
     git push origin main
     ```

     Only if you're **certain** no one else has pulled (e.g., a private branch) might you reset and force-push with `--force-with-lease` — but on `main`/`develop`, revert is the correct, collaboration-safe choice.

     **[⬆ Back to Top](#table-of-contents)**

---

### Disclaimer

The questions and answers in this README are a curated summary of commonly asked Git interview questions, spanning foundational concepts through advanced and scenario-based depth. There is no guarantee that these exact questions will appear in any given interview — the purpose is to help you rapidly review key concepts and build deep understanding. Contributions and corrections are welcome.

Good luck with your interview 😊

---
