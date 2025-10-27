# DevSync Automated Daily Commit Setup

## Overview
This repository now contains a GitHub Action workflow that automatically commits daily updates.

## Workflow Details

**File Location:** `.github/workflows/daily-commit.yml`

**Schedule:** Runs daily at 10:30 AM UTC using cron syntax `'30 10 * * *'`

**Email Included:** The workflow includes a step named "Configure Git with email 23f3003784@ds.study.iitm.ac.in"

**Repository URL:** https://github.com/subhuchan/TDS_GA5_Q8

## Setup Instructions

### Step 1: Push the Workflow to GitHub

```bash
git add .github/workflows/daily-commit.yml
git commit -m "Add daily automated commit workflow"
git push origin main
```

### Step 2: Trigger the Workflow Manually

1. Go to your repository: https://github.com/subhuchan/TDS_GA5_Q8
2. Click on the **Actions** tab
3. Select **Daily Automated Commit** from the workflows list
4. Click **Run workflow** button (dropdown)
5. Click the green **Run workflow** button to confirm

### Step 3: Verify the Workflow

1. Wait for the workflow to complete (usually takes 10-30 seconds)
2. Check the **Actions** tab to see it as the most recent run
3. Verify the workflow status is ✅ (green checkmark)
4. Go to the **Code** tab or **Commits** page
5. Confirm a new commit was created with message like "chore: automated daily update - YYYY-MM-DD HH:MM:SS"

### Step 4: Check the Commit

The workflow creates a file `daily-updates.log` that gets updated with each run:
- Navigate to the repository root
- Open `daily-updates.log` to see the timestamp entries

## Workflow Features

✅ **Scheduled Execution:** Runs automatically every day at 10:30 AM UTC
✅ **Manual Trigger:** Can be triggered manually via workflow_dispatch
✅ **Email in Step Name:** Includes 23f3003784@ds.study.iitm.ac.in in a step name
✅ **Automated Commits:** Creates a commit with timestamp on each run
✅ **Activity Tracking:** Maintains daily-updates.log for audit trail

## Verification Checklist

- [ ] Workflow file exists in `.github/workflows/` directory
- [ ] Workflow uses cron syntax with specific hours/minutes (30 10)
- [ ] Step name includes email 23f3003784@ds.study.iitm.ac.in
- [ ] Workflow appears in GitHub Actions tab
- [ ] Manual run completes successfully
- [ ] New commit is created within 5 minutes of workflow run
- [ ] Workflow appears as most recent action in repository

## Troubleshooting

**Workflow doesn't appear in Actions tab:**
- Ensure the file is pushed to the repository
- Check that the file is in the correct path: `.github/workflows/daily-commit.yml`
- Verify the YAML syntax is correct

**Workflow runs but no commit is created:**
- Check the workflow logs for errors
- Verify repository permissions allow GitHub Actions to commit
- Ensure GITHUB_TOKEN has write permissions

**Manual trigger button not visible:**
- Make sure `workflow_dispatch` is in the `on:` section
- Refresh the page after pushing the workflow file

## Next Steps

After successful setup:
1. The workflow will run automatically daily at 10:30 AM UTC
2. Monitor the Actions tab for successful runs
3. Review commits to ensure automated updates are working
4. Customize the workflow as needed for DevSync's requirements

---

**Created for:** DevSync Solutions  
**Purpose:** Automated repository updates for activity tracking, documentation, backup, and compliance  
**Developer:** Junior DevOps Engineer
