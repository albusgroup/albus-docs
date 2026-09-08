# Docs audit (working notes)

Working branch for the docs audit. Not meant to merge as-is; this file is removed before merge.

## How to leave feedback

1. Open any `.mdx` page on GitHub on this branch, click edit, and add a comment where you want a change:

   ```mdx
   {/* TODO(carlo): this section is outdated, mention invocation keys */}
   ```

   Comments are invisible on the rendered site. Commit directly to this branch.

2. Or leave an inline review comment on this PR.

Devin sweeps the `TODO(carlo)` comments, applies the change, removes the marker, and replies on the PR with what was done per page.

## Requested changes (round 1)

Markers `{/* TODO(n): ... */}` in each page reference these numbers.

1. Remove all private beta/alpha references; drop the `docs.json` banner, the "Private beta" nav group, and the `/alpha/*` redirects.
2. Remove "Get access" (`getting-started/access.mdx`) and its nav entry.
3. Remove "Install" (`getting-started/install.mdx`); fold the install one-liner into Authentication.
4. Getting started = two pages: "Albus" (`index.mdx`) and "Authentication" (`getting-started/authenticate.mdx`). DECIDED: merge `first-session.mdx` into `index.mdx`.
5. Remove the "For coding agents" group and `getting-started/for-your-agent.mdx`. DECIDED: `agents/docs.mdx` stays live at its URL (the CLI prints it) but leaves the nav; strip beta wording.
6. CLI reference — DECIDED: keep, trimmed to a command → flags table (see below).
7. Remove "Documentation release policy" (`guides/releases.mdx`).
8. Remove "API reference" (`reference/overview.mdx`); Reference group = SDKs, Errors (+ CLI if kept). The generated OpenAPI "API reference" group stays.
9. Rename "Use your own model key" to "Bring your own key" (`guides/model-providers.mdx`).

### On 6 (CLI reference)

Recommendation: keep it, but make it lean. It is the only place flags, env vars, and exit codes are enumerated, and `albus login` is the only browser sign-in path, so Authentication will link into it. Cut the per-command prose down to a table (command → API operation → flags) and delete anything the `--help` output already says. If you'd rather drop it, the Authentication page needs to absorb `login`/`tokens create`, and the SDK page needs the `sessions run` example.

## Page checklist

- [ ] index.mdx
- [ ] getting-started/access.mdx
- [ ] getting-started/install.mdx
- [ ] getting-started/authenticate.mdx
- [ ] getting-started/first-session.mdx
- [ ] getting-started/for-your-agent.mdx
- [ ] guides/run-a-session.mdx
- [ ] guides/agents-and-revisions.mdx
- [ ] guides/model-providers.mdx
- [ ] guides/mcp-servers.mdx
- [ ] guides/secrets.mdx
- [ ] guides/audit-log.mdx
- [ ] guides/releases.mdx
- [ ] guides/troubleshooting.mdx
- [ ] reference/overview.mdx
- [ ] reference/cli.mdx
- [ ] reference/sdks.mdx
- [ ] reference/errors.mdx
- [ ] agents/docs.mdx
- [ ] beta/limitations.mdx
- [ ] beta/support.mdx
