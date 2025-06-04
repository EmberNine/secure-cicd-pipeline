# Secure CI/CD Pipeline with GitHub Actions

## Goal
This project demonstrates a secure CI/CD pipeline that includes:

- Static Application Security Testing (CodeQL)
- Secrets scanning (Gitleaks)
- Dependency scanning (Trivy or Snyk)
- Docker image scanning
- Optional deployment logic

## Folder Structure
- `.github/workflows/ci.yml`: The secure CI/CD pipeline definition.
- `src/`: Contains a sample Python app.
- `Dockerfile`: Used to build a container image for the app.
- `.gitleaks.toml`: Config for secrets scanning.

## Running Locally

1. Install Python, Docker, and Trivy or Snyk
2. Clone this repo
3. Run: `pip install -r requirements.txt`
4. Build and scan:
   ```bash
   docker build -t myapp .
   trivy image myapp
   ```

## GitHub Setup

- Enable GitHub Actions in your repo.
- Push code to trigger the `ci.yml` workflow.
- You’ll see results under the **Actions** tab.

## 🛡️ Security Checks
| Check Type      | Tool        |
|------------------|-------------|
| SAST             | CodeQL      |
| Secrets Scanning | Gitleaks    |
| Dependency Scan  | Trivy / Snyk|
| Image Scan       | Trivy       |
