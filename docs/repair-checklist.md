# Maticaws Repair Checklist

This file tracks the intended repair path for the original `Maticaws/` CTO source dump.

## Completed

- Added a Hardhat project scaffold with `package.json`.
- Added `hardhat.config.js`.
- Added `.gitignore`.
- Expanded the title-only README into a status-focused project README.
- Added `docs/status.md`.
- Preserved the original `Maticaws/` source dump.

## Confirmed original source issues

- `Maticaws/contracts/Maticaws.sol` imports OpenZeppelin using the standard npm package layout.
- The vendored OpenZeppelin files in `Maticaws/@openzeppelin/` do not fully match that import layout.
- `Maticaws/@openzeppelin/contracts/access/Ownable.sol` is empty.
- `Maticaws/@openzeppelin/contracts/security/Pausable.sol` is empty.
- No complete package/tooling setup was originally present.
- No tests were originally present.
- The free-mint reset logic needs review because the original claim check can allow repeated claims in reset mode.
- The owner-only `safeMint` function needs a max-supply check.
- The BOGO mint path should calculate total minted amount before minting.
- Withdrawal should use a call pattern rather than `transfer` for better compatibility with contract owners.

## Intended next code changes

- Add a repaired active contract at `contracts/Maticaws.sol` using OpenZeppelin Contracts 4.x from npm.
- Add tests under `test/Maticaws.test.js`.
- Keep the original `Maticaws/` folder as archival source material.
- Run `npm install`.
- Run `npm run compile`.
- Run `npm test`.

## Manual review required

Before deployment, confirm:

- Whether token IDs should start at `0` or `1`.
- Whether the free-mint round boundaries are intentional.
- Whether exact payment should be required or overpayment should be accepted.
- Whether owner minting should allow custom token URIs.
- Whether metadata at `https://api.maticaws.club/metadata/` still exists and matches token ID format.

## Status

The repository is safer and better documented, but the repaired Solidity source and tests still need to be added and validated before the project can be considered fixed.
