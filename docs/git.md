# Git Submodule Management

This document provides instructions on how to manage Git submodules in your project.

## Adding a Submodule

To add a new submodule to your repository, use the following command:

```bash
git submodule add <repository_url> <path_to_submodule>
```

> Replace `<repository_url>` with the URL of the repository you want to add as a submodule, and `<path_to_submodule>` with the directory path where you want to place the submodule.

## Cloning a Repository with Submodules

When cloning a repository that contains submodules, use the `--recursive` option to ensure all submodules are cloned as well:

```bash
git clone --recursive <repository_url>
```

> Replace `<repository_url>` with the URL of the repository you want to clone.

If you have already cloned the repository without the `--recursive` option, you can initialize and update the submodules with the following commands:

```bash
git submodule init
git submodule update
```

Alternatively, you can use a single command to initialize and update all submodules:

```bash
git submodule update --init --recursive
```

## Updating Submodules

To update all submodules to their latest commit on the specified branch, use:

```bash
git submodule update --remote --merge
```

> This command fetches the latest changes from the remote repositories of the submodules and merges them into your current branch.
> You can also update a specific submodule by navigating to its directory and pulling the latest changes:

```bash
cd <path_to_submodule>
git pull origin <branch_name>
```

> Replace `<path_to_submodule>` with the path to the submodule and `<branch_name>` with the branch you want to pull from.

## Removing a Submodule

```bash
git submodule deinit <path_to_submodule>
git rm <path_to_submodule>
rm -rf .git/modules/<path_to_submodule>
```

> Replace `<path_to_submodule>` with the path to the submodule you want to remove.
