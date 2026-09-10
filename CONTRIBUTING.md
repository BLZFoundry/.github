# How BLZ Foundry checks in work

This is the plain-English workflow for changing a BLZ Foundry project. The goal is simple: anyone should be able to understand what happened, confirm it works, and continue the work later.

## The short version

1. **Create a branch.** This is a temporary work lane that keeps unfinished changes away from the trusted version.
2. **Make one focused change.** Smaller changes are easier to understand, test, and undo.
3. **Create a commit.** A commit is a named checkpoint of the files you changed.
4. **Open a pull request (PR).** The PR is the check-in: what was done, why, how, what changed, proof it works, and how to pick it up.
5. **Review it in plain language.** Someone unfamiliar with the work should understand the 30-second version.
6. **Merge it.** Merging puts the approved change into `main`, the project's trusted current source.
7. **Release it when needed.** A merge does not always make a change live. Record the deployment or live URL in the PR.

## Branch names

Use a short name that says what kind of work is happening:

- `feature/short-purpose` for new capability
- `fix/short-purpose` for a correction
- `docs/short-purpose` for documentation
- `experiment/short-purpose` for a test or proof

Automated Codex branches may use the `codex/` prefix.

## What a good PR answers

A useful PR lets another person answer these questions without reconstructing the whole conversation:

- What did we do?
- Why did we do it?
- What changed for a user or operator?
- How was it done?
- What proves it works?
- What could go wrong or still needs attention?
- Where should the next person start?
- Is it live, ready to release, or documentation only?

The organization PR template asks these questions automatically. Keep the answers direct. If a section does not apply, say `Not applicable` instead of deleting it.

## Tiny example

**What did we do?** Added the BLZ Foundry About page and connected it to the main navigation.

**How do we know it works?** Opened the production URL on desktop and mobile, checked every link, and confirmed the build passed.

**How does someone pick this up?** Start in `src/pages/about`, run the local site, then review the open copy notes in the PR.

**Release impact:** Released at the linked production URL.

## The five words worth knowing

- **Repository (repo):** the project, its files, and its history.
- **Branch:** a temporary lane for a change.
- **Commit:** a saved checkpoint.
- **Pull request (PR):** the explanation and review before a change joins the trusted version.
- **Merge:** accepting the reviewed change into `main`.

When in doubt, write for future you.
