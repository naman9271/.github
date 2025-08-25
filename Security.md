<!--security-start-->
## Security Announcements

Join the [kubestellar-security-announce](https://groups.google.com/u/1/g/kubestellar-security-announce) group to receive emails about security and major API announcements.

## Dependency Policy

KubeStellar manages dependencies under the following policy:

- **Dependency Detection:** We use [Dependabot](https://github.com/dependabot) to automatically check and propose updates for Go modules, Python requirements, Dockerfiles, Helm charts, and GitHub Actions workflows. Dependabot PRs serve as prompts but are not merged automatically.
- **Update Process:** After Dependabot creates a PR, maintainers allow time for potential issues to surface before proceeding. Handling depends on the dependency type:
  - **GitHub Actions:** Maintainers create their own PRs, following our [GitHub Action reference discipline](https://github.com/kubestellar/kubestellar/blob/main/CONTRIBUTING.md#github-action-reference-discipline) and established practices.
  - **Go Dependencies:** If the Dependabot PR works as-is, it may be accepted directly. If not, maintainers open their own PR to fix or adapt the update.
- **Review Process:** All dependency update PRs undergo the same [review process](https://github.com/kubestellar/kubestellar/blob/main/CONTRIBUTING.md#pull-requests) as any code change. Maintainers ensure updates do not introduce breaking changes or vulnerabilities before merging.
- **Vulnerability Checking:** Before merging, maintainers perform security checks:
  - **Security Scanning:** KubeStellar imports multiple dependency types (Go packages, binaries, container images, Helm charts, GitHub Actions). We rely on GitHub’s advisory database and Dependabot’s detection features. No single standardized tool is used across all dependency types.
  - **Advisory Review:** Maintainers review release notes and advisories for updated dependencies.
  - **Breaking Changes:** Updates are checked for compatibility issues.
  - **GitHub Actions:** Updates must follow the [Action Reference Discipline](https://github.com/kubestellar/kubestellar/blob/main/CONTRIBUTING.md#github-action-reference-discipline) and use approved commit hashes. The [verify-action-hashes workflow](https://github.com/kubestellar/kubestellar/blob/main/.github/workflows/verify-action-hashes.yaml) enforces this automatically.
  - **SBOM Generation:** We generate a Software Bill of Materials (SBOM) using [Anchore's syft tool](https://github.com/kubestellar/kubestellar/blob/main/.github/workflows/goreleaser.yml) during releases to track dependencies for security analysis.
  - **Testing:** All available tests are run to ensure updated dependencies work correctly with the codebase.
- **Best Practices:** We avoid unmaintained or deprecated dependencies. Security advisories are monitored via GitHub’s advisory database and Dependabot alerts. Any vulnerabilities are prioritized for prompt remediation.
- **Documentation:** The dependency update process is documented in the repository’s README and CONTRIBUTING guidelines.

## Reporting a Vulnerability

We greatly appreciate security researchers and users who report vulnerabilities to the KubeStellar Open Source Community. All reports are thoroughly investigated by community volunteers.

To report, email [kubestellar-security-announce@googlegroups.com](mailto:kubestellar-security-announce@googlegroups.com) with details, following the expectations for [KubeStellar bug reports](https://github.com/kubestellar/kubestellar/blob/main/.github/ISSUE_TEMPLATE/bug_report.yaml).

### When to Report
- You believe you found a potential security vulnerability in KubeStellar  
- You are unsure how a vulnerability impacts KubeStellar  
- You found a vulnerability in a dependency KubeStellar uses  
  - If the dependency has its own reporting process, please report it there directly

### When *Not* to Report
- You need help tuning KubeStellar for security  
- You need help applying security updates  
- The issue is not related to security  

## Security Vulnerability Response

Each report is acknowledged and analyzed within **3 working days**.  

All vulnerability details shared with the Security Response Committee remain private to KubeStellar unless disclosure is needed to resolve the issue.  

As the issue moves from triage → fix → release planning, we keep the reporter updated.

## Public Disclosure Timing

A disclosure date is agreed upon between the reporter and the Security Response Committee.  
We prefer to disclose as soon as mitigation is available, but may delay if the fix is not yet well-understood, tested, or requires vendor coordination.  

- **Typical timeframe:** immediate to a few weeks  
- **Straightforward mitigations:** usually disclosed within ~7 days  

The KubeStellar maintainers have the final decision on disclosure timing.
<!--security-end-->
