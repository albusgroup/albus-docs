# Albus documentation

This public repository contains hand-authored guides and the OpenAPI snapshot
used to render the production API reference at `docs.albus.com`.

Mintlify is installed only on this repository and deploys pushes to `master`.
It has no access to the private `albusgroup/albus` source repository. The
private repository's release workflow uses an internal GitHub App to promote
the already-deployed OpenAPI snapshot.

## Release procedure

1. Deploy the matching backend revision to production.
2. Run the private repository's `Publish API documentation` workflow with that
   revision and the released `albus-sdk` version.
3. The workflow updates `openapi/openapi.yaml` and the release metadata here.
4. Mintlify publishes the resulting `master` commit.

Do not copy an OpenAPI specification from an unmerged or undeployed revision
into this repository.
