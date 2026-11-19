# 🚀 Secure CI/CD Pipeline Project

This repository demonstrates a complete, automated CI/CD pipeline built with GitHub Actions. It is designed to enforce code quality, run security scans, and prevent bad code from reaching the `main` branch.

## 🛠️ Features Built

*   **Continuous Integration (CI):** Automated validation workflows run on every Pull Request to ensure basic tests pass.
*   **DevSecOps (OWASP Top 10):** Integrated GitHub CodeQL to automatically scan code for security vulnerabilities (like Cross-Site Scripting and SQL Injection).
*   **Branch Protection:** Enforced strict rulesets on the `main` branch. Direct pushes are blocked, and all Pull Requests require passing status checks.
*   **Approval Gates:** The pipeline physically blocks the merge button if automated tests or security scans fail.

## ⚙️ How the Pipeline Works

1.  **Developer creates a Pull Request:** Code is proposed via a new branch.
2.  **Automated Tests Run:** The `ci.yml` workflow runs validation tests.
3.  **Security Scan Runs:** The `security.yml` workflow executes CodeQL analysis to find vulnerabilities.
4.  **The "Locked Door":** GitHub's branch protection checks if both robots succeeded.
5.  **Merge:** If and only if all checks pass, the code is allowed to be merged into `main`.

## 🚦 Status Badges
![CI Validation](https://github.com/vaino118/cicd-pipeline-project/actions/workflows/ci.yml/badge.svg)
![OWASP Security Scan](https://github.com/vaino118/cicd-pipeline-project/actions/workflows/security.yml/badge.svg)
