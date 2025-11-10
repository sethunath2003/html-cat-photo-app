# 🤖 GitHub Automation

This folder contains the GitHub-specific configurations and automations for the Cat Photo App repository.

## 📁 Contents

### Workflows (`.github/workflows/`)

#### 1. `validate-contribution.yml`
**Triggers:** When a PR is opened/updated that modifies files in `submissions/`

**What it does:**
- Welcomes new contributors
- Validates submission structure
- Checks for required files (index.html, README.md)
- Verifies folder naming conventions
- Posts detailed validation reports
- Adds appropriate labels (contribution, ready-for-review, needs-changes)

**Why it's helpful:** Provides immediate automated feedback to contributors, reducing moderator workload and helping contributors fix issues quickly.

#### 2. `greet-first-time.yml`
**Triggers:** When a first-time contributor opens an issue or PR

**What it does:**
- Detects first-time contributors
- Posts a welcoming message
- Provides helpful links and next steps

**Why it's helpful:** Creates a welcoming environment and guides new contributors to useful resources.

#### 3. `setup-labels.yml`
**Triggers:** Manual trigger or when pushed to main

**What it does:**
- Creates/updates standard labels for the repository
- Ensures consistent labeling across issues and PRs

**Why it's helpful:** Maintains organized issue and PR tracking.

### Templates

#### `PULL_REQUEST_TEMPLATE.md`
Pre-filled template that appears when contributors create a PR. Includes:
- Submission checklist
- Required information fields
- Learning experience questions
- Guidelines reminder

#### `CODEOWNERS`
Defines moderators who are automatically requested for review on PRs affecting:
- Submissions
- Documentation
- GitHub configurations

### Issue Templates (`ISSUE_TEMPLATE/`)

#### `question.yml`
For general questions about:
- Building the Cat Photo App
- Setting up GitHub Pages
- Contribution process
- Git/GitHub usage

#### `bug_report.yml`
For reporting bugs in:
- Documentation
- Bot behavior
- Repository structure

#### `feature_request.yml`
For suggesting:
- Documentation improvements
- New tutorial sections
- Bot enhancements
- Repository improvements

## 🔧 Configuration

### Permissions Required

The workflows require the following permissions:
- `pull-requests: write` - To comment on PRs
- `issues: write` - To comment on issues and manage labels
- `contents: read` - To read repository contents

These are configured in each workflow file.

### Secrets

No secrets are required! All workflows use the default `GITHUB_TOKEN` provided automatically by GitHub Actions.

## 🎯 How the Bot Helps

### For Contributors:
1. **Immediate Feedback** - Know instantly if submission structure is correct
2. **Clear Instructions** - Get specific guidance on what to fix
3. **Welcoming Experience** - Feel supported throughout the process
4. **Learning Opportunity** - Understand requirements through automated checks

### For Moderators:
1. **Pre-validation** - Only review PRs that pass basic checks
2. **Time Saving** - Don't need to manually check folder structure
3. **Consistent Standards** - Automated checks ensure uniform requirements
4. **Clear Status** - Labels make it easy to see PR status at a glance

## 🧪 Testing the Automation

### Test the Validation Bot:
1. Create a test PR with a sample submission
2. Try both correct and incorrect folder structures
3. Verify the bot comments and labels appropriately

### Test Label Setup:
1. Manually trigger the `setup-labels.yml` workflow
2. Check that all labels are created in the repository

### Test First-Time Greeting:
1. Have a new contributor open an issue or PR
2. Verify they receive a welcoming message

## 🔄 Modifying the Automation

### To change validation rules:
Edit `.github/workflows/validate-contribution.yml` in the "Validate submission structure" step.

### To modify the welcome message:
Edit `.github/workflows/validate-contribution.yml` in the "Welcome new contributor" step.

### To add/remove labels:
Edit `.github/workflows/setup-labels.yml` and add/remove from the `labels` array.

### To update issue templates:
Edit the corresponding `.yml` file in `.github/ISSUE_TEMPLATE/`

## 📚 Additional Resources

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [GitHub Script Action](https://github.com/actions/github-script)
- [Issue Form Schema](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)
- [CODEOWNERS Syntax](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)

## 💡 Pro Tips

1. **Test locally first**: Use [act](https://github.com/nektos/act) to test workflows locally
2. **Check logs**: View workflow runs in the Actions tab for debugging
3. **Be descriptive**: Use clear commit messages when modifying workflows
4. **Document changes**: Update this README when adding new automation

## 🐛 Troubleshooting

### Bot not responding to PRs:
- Check if the PR modifies files in `submissions/`
- Verify workflow has necessary permissions
- Check Actions tab for error logs

### Labels not being added:
- Ensure labels exist (run setup-labels workflow)
- Check workflow permissions
- Verify syntax in workflow file

### Templates not appearing:
- Ensure file names match exactly (including `.yml` extension)
- Check YAML syntax is valid
- Clear browser cache and refresh

---

**Questions about the automation?** Open an issue with the "question" label!
