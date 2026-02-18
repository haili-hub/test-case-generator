# GitHub Actions Workflow Guide

## Overview
This repository includes a GitHub Actions CI workflow located at `.github/workflows/blank.yml` that automatically runs tests and validations.

## Workflow Triggers

The CI workflow is triggered by:
1. **Push events** to the `main` branch
2. **Pull request events** targeting the `main` branch
3. **Manual trigger** via the Actions tab (workflow_dispatch)

## Workflow Jobs

The workflow includes a single job called `build` that runs on `ubuntu-latest` and performs the following steps:

1. **Checkout code**: Uses `actions/checkout@v4` to clone the repository
2. **Run hello world**: Executes a simple echo command
3. **Run multi-line script**: Demonstrates multi-line command execution
4. **Run test script**: Executes the `test-example.sh` validation script

## Running the Workflow

### Automatic Execution
The workflow runs automatically when:
- Code is pushed to the `main` branch
- A pull request is opened or updated targeting `main`

### Manual Execution
To manually trigger the workflow:
1. Go to the repository on GitHub
2. Click on the **Actions** tab
3. Select the **CI** workflow from the left sidebar
4. Click **Run workflow** button
5. Select the branch and click **Run workflow**

## Workflow Status

You can view workflow runs and their status in the **Actions** tab of the GitHub repository.

## Test Script

The `test-example.sh` script validates that the CI workflow is operational. It:
- Prints validation messages
- Confirms successful execution
- Exits with code 0 on success

## Notes

- Pull requests from bot accounts may require approval from a repository maintainer before the workflow runs (GitHub security feature)
- Workflow runs on the `main` branch execute automatically without approval
- You can view detailed logs for each workflow run in the Actions tab
