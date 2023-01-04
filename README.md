# npm-publish-workflow

Since the process of deploying any npm package to npmjs.com is essentially the same across all packages, this reusable workflow in .github/workflows/npm-publish-workflow.yml centralizes all of the testing and deployment logic in one place to avoid having to copy/paste the workflow in all npm package GitHub repositories.

## Usage

```
name: Node.js Package

on:
  push:

jobs:
  build:
    uses: jamesmortensen/npm-publish-workflow/.github/workflows/npm-publish-workflow.yml@main
```

NOTE: The repository calling the workflow must set the NPM_TOKEN secret in GitHub Actions secrets.

