<!-- Licensed under CC-BY 4.0. -->

# Release Preparation Checklist

## Purpose
Ensure the repository is ready for a production release.

## Prerequisite
Run the **Weekly Maintenance Checklist** before starting these tasks.

## Steps
- Verify versioning and `CHANGELOG` updates; confirm semantic version bump.
- Provide migration notes and deprecation warnings where needed.
- Execute a clean-room build and run E2E and smoke tests on all target OS/architectures.
- Perform packaging checks: signing, attach SBOM, ensure license headers.
- Finalize release notes; regenerate and publish the docs site.

## Output
- Confirmation that release tasks are complete.
- Notes on any remaining issues.

## Acceptance Criteria
- Version and changelog accurately reflect changes.
- Clean-room build and tests succeed on all targets.
- Packaging and documentation steps completed.

## Validation Checklist
- [ ] Version and `CHANGELOG` updated.
- [ ] Migration notes and deprecation warnings provided.
- [ ] Build and tests run on all targets.
- [ ] Packaging, signing, and SBOM steps completed.
- [ ] Release notes finalized and docs published.
