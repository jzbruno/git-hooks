# Git Hooks

## Overview

This repo contains Git hooks that can be run before commits to help validate

- Style
- Linting
- Build
- Test

The *pre-commit* hook will run all other *pre-commit-\** hooks.

## Requirements

- Git >= 2.9
- Terraform (pre-commit-terraform)

## Usage

1. Add this repo as a sub module to the repo you would like to use the Git hooks for.

    ```bash
    cd <external-repo-path>
    git submodule add https://github.com/jzbruno/git-hooks.git hooks/
    ```

2. Enable *pre-commit* hooks by removing the *.disabled* from the filename.

3. Configure the sub module as the Git hooks path for the external project. Each team member needs 
to do this when they clone the repo.

    ```bash
    git config core.hooksPath hooks
    ```
