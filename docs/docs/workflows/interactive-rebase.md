# Interactive rebase

When you are working on a branch, you may want to reorganize your commits.
Usually, the branch you are working on is not the `main` branch, but a feature
branch. Following conventional commits, your branch should be associated with a
feature, a bug fix, or a chore. So before merging your branch into the `main`
branch, you usually want to squash your commits into one or a few commits, and
keep only one type of commit (e.g. only `feat` commits).

## TLDR

The usual workflow looks like this:

1. git checkout main
2. git pull
3. git checkout <your-branch>
4. git rebase -i main
5. Squash commits
6. git push --force-with-lease

For more details, see the sections below.

## What is an interactive rebase?

An interactive rebase is a way to reorganize your commits. It allows you to
reorder your commits, squash commits, and edit commit messages.

## Usage

Usually, when working on a PR, you will want to rebase your branch on top of the
latest changes in the `main` branch, and then squash your commits to keep only a
few commits.

To rebase your branch on top of the latest changes in the `main` branch, run the
following command:

```bash
> git checkout main
> git pull
> git checkout <your-branch>
> git rebase -i main
[-i is for interactive]
```

In the editor you can then squash the commits you want to squash, and reorder
the commits you want to reorder.

## Squashing commits

In the editor, you can squash commits by changing `pick` to `squash` or `s`:

```bash
pick 1a2b3c4 Add a new feature
squash 4d5e6f7 Fix a bug
squash 7g8h9i0 Fix another bug
```

## Pushing your changes

After you have rebased your branch, you will need to force push your changes to
the remote branch:

```bash
> git push --force-with-lease
```

The option `--force-with-lease` is safer than `--force` because it will fail if
the remote branch has changed since you last pulled it.
