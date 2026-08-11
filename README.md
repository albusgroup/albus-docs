# Albus documentation

This public repository contains hand-authored guides and the OpenAPI snapshot
used to render the production API reference at
[docs.albus.sh](https://docs.albus.sh).

Two pages are written for coding agents rather than people and are linked by
exact URL from the CLI, the SDK READMEs, and the console:

| Page | URL agents are given |
|---|---|
| `agents/docs.mdx` | https://docs.albus.sh/agents/docs.md |

One page, deliberately: an agent given a URL reads that URL and rarely follows
links, so setup, the API surface, the rules, and the examples all live there.
Keep it imperative, complete, and executable end to end — it is the target of
"read this and use Albus", so a step that is wrong there is a failed setup, not a
confusing paragraph — and keep it in sync with the CLI's actual commands and
error strings.

Mintlify is installed only on this repository and deploys pushes to `master`.
It has no access to the private `albusgroup/albus` source repository. The
private repository's release workflow uses a GitHub Actions secret named
`ALBUS_DOCS_PUBLISH_TOKEN` to promote the already-deployed OpenAPI snapshot.

## Release procedure

1. Deploy the matching backend revision to production.
2. Run the private repository's `Publish API documentation` workflow with that
   revision and the released `albus-sdk` version.
3. The workflow updates `openapi/openapi.yaml` and the release metadata here.
4. Mintlify publishes the resulting `master` commit.

Do not copy an OpenAPI specification from an unmerged or undeployed revision
into this repository.
