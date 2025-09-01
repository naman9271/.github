# GitHub Workflow Templates

This directory contains reusable GitHub Actions workflow templates that can be used across your organization's repositories.

## Available Templates

### 1. Add Good First Issue Label (`add-good-first-issue-labels.yml`)
Automatically adds the "good first issue" label when users comment `/good-first-issue` on issues.

**Usage:** Just add this workflow to any repository and it will work automatically when maintainers comment on issues.

### 2. Add Help Wanted Issue Label (`add-help-wanted-issue-labels.yml`)
Automatically adds the "help wanted" label when users comment `/help-wanted` on issues.

**Usage:** Just add this workflow to any repository and it will work automatically when maintainers comment on issues.

### 3. Assignment Helper (`assignment-helper.yml`)
Helps users who make natural language assignment requests by guiding them to use proper slash commands like `/assign`.

**Customization Required:**
- Update the Contributors Guide URL in the response message to match your repository

### 4. Greetings for New Contributors (`greeting.yml`)
Welcomes new contributors when they open their first issue or pull request.

**Customization Required:**
- The workflow automatically uses `${{ github.repository }}` variables, but you may want to customize the welcome messages
- Update community discussion links if needed

### 5. Close Stale Issues and PRs (`stale.yml`)
Automatically marks and closes stale issues and pull requests to keep your repository organized.

**Customization Options:**
- `days-before-stale`: Number of days before marking as stale (default: 45)
- `days-before-close`: Number of days after being stale before closing (default: 10)
- `exempt-issue-labels` and `exempt-pr-labels`: Labels that prevent items from being marked stale
- Customize stale and close messages

### 6. CI/CD Pipeline (`ci-cd-pipeline.yml`)
A comprehensive CI/CD pipeline template with code verification, linting, testing, and building.

**Customization Required:**
- Replace placeholder commands with your actual build/test/lint commands
- Configure appropriate setup steps for your tech stack
- Adjust build artifact paths
- Set up proper environment variables

### 7. Security Scan (`security-scan.yml`)
Comprehensive security scanning including dependency vulnerabilities, secret detection, and CodeQL analysis.

**Customization Required:**
- Update the `language` matrix in the CodeQL job to match your project languages
- Configure manual build steps if autobuild fails
- Adjust scan schedules as needed

### 8. Release Automation (`release-automation.yml`)
Automated release workflow with changelog generation, multi-platform builds, Docker images, and asset uploads.

**Customization Required:**
- Update build commands for your specific technology stack
- Configure build matrix for your target platforms
- Set up Docker builds (optional)
- Configure package publishing (optional)
- Add notification integrations

### 9. Dependency Updates (`dependency-updates.yml`)
Automated dependency updates for multiple programming languages with security advisory checking.

**Features:**
- Supports Node.js, Go, Python, and Rust projects
- Creates pull requests with dependency updates
- Enables Dependabot vulnerability alerts
- Runs weekly or on-demand

**Customization Options:**
- Adjust the schedule frequency
- Modify dependency update strategies per language
- Configure additional package managers

## How to Use These Templates

### Option 1: Organization-wide Templates
If this is an organization `.github` repository, these templates will automatically appear in the "Actions" tab of all repositories in your organization under "Templates".

### Option 2: Manual Copy
1. Copy the desired `.yml` file to your repository's `.github/workflows/` directory
2. Customize the workflow according to the instructions above
3. Commit and push the changes

### Option 3: Template Repository
You can also create a template repository with these workflows pre-configured.

## Template Structure

Each template consists of:
- `*.yml` - The actual workflow file
- `*.properties.json` - Metadata for the template (name, description, icon, categories)

## Contributing

When adding new templates:
1. Create both the `.yml` workflow file and corresponding `.properties.json` file
2. Add documentation to this README
3. Test the workflow in a sample repository
4. Include clear customization instructions

## Best Practices

- Always include `workflow_dispatch` trigger for manual testing
- Use appropriate permissions (principle of least privilege)
- Include clear comments in workflows for customization points
- Use the latest stable versions of actions
- Include error handling where appropriate
- Add meaningful job and step names
