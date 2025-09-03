# Release Preparation Checklist

Run the **Weekly Maintenance Checklist**. Before each release, also:

- Verify versioning and `CHANGELOG` updates; confirm semantic version bump.
- Provide migration notes and deprecation warnings where needed.
- Execute a clean-room build and run E2E and smoke tests on all target OS/architectures.
- Perform packaging checks: signing, attach SBOM, ensure license headers.
- Finalize release notes; regenerate and publish the docs site.
