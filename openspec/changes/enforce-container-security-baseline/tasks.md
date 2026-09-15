## 1. Runtime and dependencies

- [ ] 1.1 Move the image to the pinned Java 21 LTS multistage runtime and preserve the `/jenkins` health contract
- [ ] 1.2 Pin plugins and direct Python dependencies, use the copied virtual environment, and keep all helpers executable
- [ ] 1.3 Minimize runtime packages and install checksum-verified amd64/arm64 `kubectl`

## 2. Container security gate

- [ ] 2.1 Add complete HIGH/CRITICAL reporting and a blocking CRITICAL scan to both platform jobs
- [ ] 2.2 Keep accepted findings visible and constrain every exception by package, rationale, owner, tracking issue, and original expiry

## 3. Validation

- [ ] 3.1 Run OpenSpec, dependency, workflow, and repository validation
- [ ] 3.2 Build and smoke-test amd64 and arm64 images and confirm no unaccepted CRITICAL finding passes
- [ ] 3.3 Validate the Jenkins `/jenkins` runtime and NITA job helpers in an isolated integration environment
