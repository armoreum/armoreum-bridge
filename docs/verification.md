# Verification

Command: `npm test` with Node.js 24.13.0 and ethers 6.17.0 available in the isolated validation environment.

**17 tests passed; 0 failed or skipped.** Checks cover explorer formatting, submission-registration retries, bounded wallet errors, and mocked LayerZero Scan responses/route attribution.

All relative Solidity imports in the extracted source resolve to copied files. External Solidity dependencies remain upstream packages. Full contract compilation, invariant tests, live bridging, operator activation, and deployed configuration were not verified by these helper tests.

Copied source digests match `SOURCE_MANIFEST.json`. Explicit dependency versions exist in the package registry and were not marked deprecated when checked. Review [NOTICE.md](../NOTICE.md) before redistribution or deployment; package metadata includes LZBL/BUSL upstream license declarations.
