# Script-Pro generation plugins

Signed catalog for downloadable generation providers. A publisher can ship separate plugins or one plugin containing several providers.

| Plugin | Provider | Release |
| --- | --- | --- |
| [Flow Google](https://github.com/2noScript/sp-gen-flow-google) | FLOW_GOOGLE | 0.1.2 preview |
| [Vibes](https://github.com/2noScript/sp-gen-vibes) | VIBES | 0.1.2 preview |

[Download SDK](https://github.com/2noScript/sp-gen-sdk/releases/tag/v0.1.1). The SDK is distributed as a GitHub release tarball; it is not yet published to npm.

The catalog is signed with Ed25519. Script-Pro ships the public verification key. Installers verify the catalog signature, exact package manifest, and SHA-256 before executing a bundle. The signing private key stays outside this repository.

- Catalog: [catalog.json](https://github.com/2noScript/sp-gen-plugins/releases/latest/download/catalog.json)
- Key: [public-key.pem](./public-key.pem)

Provider releases are previews. Live sign-in and generation require the user's provider account and remain to be verified. Google may reject authentication in embedded browsers; this release does not claim Chrome-equivalent fingerprinting or support for external OAuth callbacks.
