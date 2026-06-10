# mm-monorepo-ci-spike

Throwaway repo validating GitHub's short-circuit (always-trigger, skip-internally)
path-filtered CI pattern for per-plugin merge gating in a Mattermost-style monorepo.

Structure:
- `core/` — core code + test
- `core-plugins/plugin-a/`, `core-plugins/plugin-b/` — bundled plugins + tests
- `docs/` — docs-only changes
- `.github/workflows/ci.yml` — short-circuit CI with `dorny/paths-filter` + aggregator `gate` job
