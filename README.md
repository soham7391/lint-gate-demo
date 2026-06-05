# Lint Gate Demo

A project demonstrating a fast-fail lint gate using Git, Husky, Prettier, and GitHub Actions.

## Overview

This project prevents improperly formatted code from being committed or pushed.

The lint gate runs in two places:

1. **Local pre-commit hook (Husky)**
2. **GitHub Actions CI workflow**

If code formatting fails, the commit or CI pipeline fails immediately.

## Tech Stack

* Git
* GitHub
* Node.js
* Prettier
* Husky
* GitHub Actions

## Project Structure

```text
lint-gate-demo/
├── .github/
│   └── workflows/
│       └── lint.yml
├── .husky/
│   └── pre-commit
├── .prettierrc.json
├── index.js
├── package.json
└── README.md
```

## Installation

Clone the repository:

```bash
git clone <repository-url>
cd lint-gate-demo
```

Install dependencies:

```bash
npm install
```

## Available Commands

Check formatting:

```bash
npm run check-format
```

Automatically fix formatting:

```bash
npm run format
```

## How the Lint Gate Works

### Local Validation

When a commit is created:

```text
git commit
    ↓
Husky pre-commit hook
    ↓
npm run check-format
    ↓
PASS or FAIL
```

A failed formatting check blocks the commit.

### GitHub CI Validation

When code is pushed:

```text
git push
    ↓
GitHub Actions
    ↓
npm run check-format
    ↓
PASS or FAIL
```

A failed formatting check causes the workflow to fail.

## Learning Goals

This project was created to learn:

* Git basics
* GitHub repositories
* Commits and pushes
* Prettier formatting
* Husky pre-commit hooks
* GitHub Actions CI pipelines
* Fast-fail quality gates

```
```
