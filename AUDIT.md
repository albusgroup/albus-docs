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
