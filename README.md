# KubeStellar .github Repository

This repository contains the **default community health files** and **workflow templates** for the [KubeStellar](https://github.com/kubestellar) organization. These files are automatically inherited by all repositories within the KubeStellar organization to ensure consistency across projects.

<div align="center">
  <img src="./profile/assets/gif/enhanced_banner.gif" alt="KubeStellar Banner" height="450" width="95%">
</div>

## What is this repository?

The `.github` repository is a special repository that GitHub recognizes at the organization level. Any community health files placed here serve as defaults for all repositories in the organization that don't have their own versions of these files.

## Repository Structure

### Community Health Files
* **CODE_OF_CONDUCT.md** – Community behavior guidelines and standards
* **LICENSE** – License information for the shared community files
* **Security.md** – Security policies and vulnerability reporting procedures

### Organization Profile
* **profile/README.md** – Organization-level profile displayed on the KubeStellar GitHub page
* **profile/assets/** – Images and assets used in the organization profile

### Workflow Templates
* **workflow-templates/** – Reusable GitHub Actions workflow templates that can be used across KubeStellar repositories
  * CI/CD pipeline templates
  * Issue management workflows
  * Security scanning workflows
  * Dependency update automation
  * Release automation templates

## How to Use

### For Repository Maintainers
- These community health files will automatically apply to any KubeStellar repository that doesn't have its own version
- Workflow templates in `workflow-templates/` can be used when creating new workflows in individual repositories
- Individual repositories can override these defaults by creating their own versions

### For Contributors
- Review the CODE_OF_CONDUCT.md for community guidelines
- Check Security.md for security reporting procedures
- Refer to individual repository documentation for project-specific contribution guidelines

## Available Workflow Templates

The `workflow-templates/` directory contains ready-to-use GitHub Actions workflows:

- **CI/CD Pipeline** - Automated testing and deployment workflows
- **Issue Management** - Automated labeling and assignment helpers
- **Security Scanning** - Vulnerability scanning and security checks  
- **Dependency Updates** - Automated dependency update workflows
- **Release Automation** - Automated release and changelog generation
- **Community Management** - Greeting new contributors, stale issue management

## Contributing

Contributions to improve the organization-wide community health files and workflow templates are welcome! 

To contribute:
1. Fork this repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

Please ensure any changes maintain consistency across the KubeStellar organization and follow best practices for community health files.

## Resources

- [GitHub Community Health Files Documentation](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [GitHub Workflow Templates Documentation](https://docs.github.com/en/actions/using-workflows/creating-starter-workflows-for-your-organization)

---

Maintained by the [Kubestellar Team](https://github.com/kubestellar).
