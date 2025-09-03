# Monthly Maintenance Checklist

First complete the **Weekly Maintenance Checklist**. In addition, perform these monthly or quarterly tasks:

- Architecture review; update ADRs and diagrams; examine the dependency graph for tangles.
- Remove dead code and unused modules; plan deprecations; audit public API surface.
- Capture performance baselines and detect regressions on key paths.
- Perform a supply chain audit: build an SBOM, check license compliance, update third-party notices.
- Verify lockfiles and reproducible builds; ensure deterministic outputs.
- Check configuration and infrastructure drift across environments; maintain parity of flags and defaults.
- Review access: tokens, keys, secret rotation, least-privilege policies.
- Confirm ownership accuracy: `CODEOWNERS`, runbooks, on-call docs.
- Ensure cross-repo consistency: PR/issue templates, commit message rules, branching model.
