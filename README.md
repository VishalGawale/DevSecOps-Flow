# SecureDeploy - CI/CD with Security & Cloud Deployment

SecureDeploy is a CI/CD pipeline ensuring code quality, security, and seamless deployment to Google Cloud Run.

## Features
- **Automated Testing**: Runs `pytest` on pull requests using multiple CPUs.
- **Code Coverage**: Uses `pytest-cov` and uploads results to Codecov/Code Climate.
- **Security Scanning**: Integrates `snyk-python` for dependency security analysis.
- **Containerization**: Builds Docker images and pushes to GitHub Container Registry.
- **Cloud Deployment**: Deploys to Google Cloud Run via GitHub Actions.

## Setup
### Prerequisites
- GitHub repository, GCP account, Docker, GitHub Actions
- Secrets: `GCP_PROJECT_ID`, `GCP_SA_KEY`, `SNYK_TOKEN`

### CI/CD Workflow
1. **Pull Requests**: Runs tests, measures coverage, and performs security scans.
2. **Merge to Main**: Builds/pushes Docker images and deploys to Cloud Run.

### Deployment to Google Cloud Run
- Uses `deploy-cloudrun` GitHub Action.
- Creates `note-api-<your-org>` service.
- Configures backend to `memory`.

## Contributing
1. Ensure tests cover changes.
2. Follow security best practices.
3. Update documentation as needed.

## License
MIT License - see [LICENSE](LICENSE).
