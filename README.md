# Script-Pro generation plugins

Signed catalog for downloadable generation providers. A publisher can ship separate plugins or a package containing several providers.

| Plugin | Provider | Release |
| --- | --- | --- |
| [Flow Google](https://github.com/2noScript/plugin-sp-gen-flow-google) | FLOW_GOOGLE | 0.2.0 preview |
| [Vibes](https://github.com/2noScript/plugin-sp-gen-vibes) | VIBES | 0.2.0 preview |

[SDK 0.2.0](https://github.com/2noScript/sp-gen-sdk/releases/tag/v0.2.0) uses contract 2 and is distributed as a GitHub release tarball. Provider repositories contain independent TypeScript source and build commands; versioned archives live in their releases/ directories and GitHub Release assets.

The catalog is signed with Ed25519. Script-Pro ships the public verification key and verifies signatures, monotonic revisions, exact manifests and SHA-256 before execution. The private signing key stays outside this repository. Current catalog revision: **4**. Older provider releases remain immutable for older hosts.

- [Catalog](https://github.com/2noScript/sp-gen-plugins/releases/latest/download/catalog.json)
- [Public key](./public-key.pem)

Plugins own provider navigation, session checks and API translation. The host prefers installed Chrome through Playwright with dedicated persistent profiles. Browser requests use in-page fetch and browser-managed cookies; no exported cookie jar substitutes for the profile. WebView is a separate session, used only after Chrome startup failure or explicit selection. Native browser identity is retained without injected fingerprint overrides.

Provider releases are previews. Live Google/Meta sign-in and media generation still require verification with real accounts; installed Chrome does not guarantee anti-bot acceptance. Contract 1 tasks need an explicit update and resubmission in the contract 2 app.
