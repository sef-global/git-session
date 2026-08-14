# Git & GitHub Cheat Sheet

## The words

| Term | What it means |
|---|---|
| Repository | A project folder that remembers every version |
| Commit | A checkpoint, with a note saying why |
| Branch | A safe place to be wrong |
| `main` | The branch that should always work |
| Fork | Copy a repo into your own GitHub account |
| Clone | Copy a repo down onto your computer |
| Push | Send your commits up to GitHub |
| Pull | Bring everyone else's commits down to you |
| Pull request | Ask a maintainer to take your changes |
| Merge | Your changes become part of the project |

---

## Your first contribution (browser only, nothing to install)

1. Fork the repo — button, top right
2. Create a branch named after yourself
3. Add or edit your file in the GitHub editor
4. Commit with a message that explains the change
5. Open a pull request against the original repo
6. Reply to review comments, wait for the merge

---

## One-time setup (if you install git)

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Use the email on your GitHub account, or your commits won't be linked to your profile.

---

## The everyday loop

```bash
git pull                    # get the latest before you start
git status                  # where am I? what changed?
git add .                   # stage everything you changed
git commit -m "..."         # checkpoint, with a reason
git push                    # send it up to GitHub
```

---

## Branching

```bash
git branch                  # list branches (* = current)
git checkout -b my-fix      # new branch, switch to it
git checkout main           # switch back to main
git log --oneline           # history, newest first
```

---

## Same contribution, with git installed

```bash
git clone <your-fork-url>       # after forking on GitHub
git checkout -b my-name         # make your branch
git add .                       # stage your edit
git commit -m "Add me"          # checkpoint it
git push origin my-name         # send the branch up
```

Then open the pull request on GitHub — that step is the same either way.

---

## Commit messages

| | |
|---|---|
| Bad | `update` · `fix` · `changes` · `final v2` |
| Good | `Add Anjula to contributors page` |
| Good | `Fix broken link in README` |

---

## When something goes wrong

```bash
git status                  # always start here
git diff                    # exactly what you changed
git checkout -- <file>      # undo changes to a file
git log --oneline           # find a commit to revisit
```

---

## Habits worth keeping

- Pull before you start working. Every time.
- Commit small and often, not once at the end.
- Never commit passwords, keys or `.env` files.
- Use `.gitignore` for `node_modules` and build output.
- Ask on the issue before starting work on it.
