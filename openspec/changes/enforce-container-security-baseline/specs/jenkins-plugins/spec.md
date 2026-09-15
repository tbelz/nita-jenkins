## MODIFIED Requirements

### Requirement: Plugin list declared in version control
The system SHALL maintain `plugins.txt` with an explicit tested version for every required Jenkins plugin and install that exact set with `jenkins-plugin-cli` during the image build.

#### Scenario: Pinned plugins install at build time
- **WHEN** the Docker image is built from an unchanged `plugins.txt`
- **THEN** every named plugin is installed at its committed version without resolving an unpinned latest release
