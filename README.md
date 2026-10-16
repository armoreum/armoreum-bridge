# Armoreum Bridge

Armoreum bridge and relay contract source with submission retry, explorer formatting, and wallet-error helpers.

[MIT License](LICENSE) · [Contributing](CONTRIBUTING.md) · [Security](SECURITY.md) · [Releases](https://github.com/armoreum/armoreum-bridge/releases) · [Support](mailto:support@armoreum.io)

## Status

**Source preview extracted from actual supplied code.** This is a focused module repository, not an additional original package found in the archives. The application and full contract snapshots are preserved separately. No live service, deployment, independent audit, or registry package is claimed.

## Source modules

- `src/bridge-explorer-format.ts`
- `src/bridge-submission-queue.ts`
- `src/bridge-wallet-errors.ts`
- `src/layerzero-scan.ts`

The repository includes **10 Solidity files**, including the complete relative-import closure of the selected module. Compile with `npm run compile` after reviewing dependencies. Full Solidity compilation/integration tests are not claimed by this source extraction.

## Included bridge responsibilities

The contract source includes lock/release bridging, per-launch vaults, custom DVN and executor components, atomic destination relay, and the multichain modules present in the artifact. Required relative Solidity imports are copied recursively so local contract references are not silently dropped.

The helper source includes:

- Explorer amount/status/stage and UTC formatting.
- Durable retry registration of an already-broadcast source hash, without rebroadcasting the wallet transaction.
- Bounded extraction of user-safe wallet error messages.
- Supplementary LayerZero Scan status lookup.

The API relayer, database, provisioning worker, and live deployment records are not supplied. Scan indexing is supplementary evidence, not settlement authority. An approval, reported source hash, confirmed source lock, and destination delivery are different states.

This is not an independently operating bridge service. No live signer, deployed pair registry, private RPC URL, or funded transaction is included.

## Development and verification

Use Node.js 24 or newer and review dependencies before installation:

```sh
npm install --ignore-scripts
npm test
```

The source archive had no original dependency lockfile. Dependency versions for this module are explicit, but complete transitive resolution and audit must still be reviewed. For source inspection, the copied Node tests can also be run directly after installing their runtime dependencies in an isolated environment.

See [verification](docs/verification.md) for checks actually performed. Tests use synthetic data; no funded transaction or mainnet write is part of this verification.

## Provenance and shared code

[SOURCE_MANIFEST.json](SOURCE_MANIFEST.json) records each copied source path and checksum. Read [source scope](docs/source-scope.md). Shared code is deliberately preserved when necessary; the repository count does not imply seven independent implementations or seven running services.

## Open source and releases

Project-owned source is MIT-licensed; upstream imports retain their own licenses. GitHub Releases provide tagged source ZIP/TAR archives. `private: true` prevents accidental npm publication; it does not restrict the public source. Do not treat the source preview as an audited deployable package.

## Armoreum ecosystem

[armoreum](https://github.com/armoreum/armoreum) · [armoreum-contracts](https://github.com/armoreum/armoreum-contracts) · [armoreum-authorization](https://github.com/armoreum/armoreum-authorization) · [armoreum-recovery](https://github.com/armoreum/armoreum-recovery) · [armoreum-bridge](https://github.com/armoreum/armoreum-bridge) · [armoreum-launchpad](https://github.com/armoreum/armoreum-launchpad) · [armoreum-docs](https://github.com/armoreum/armoreum-docs)

Issues and pull requests are open. General and private security contact: **support@armoreum.io**.
