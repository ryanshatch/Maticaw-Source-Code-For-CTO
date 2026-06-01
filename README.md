# Maticaws Source Code for CTO

This repository contains a preserved Maticaws ERC-721 source-code dump for CTO / derug review.

## Current status

This repo should be treated as review material, not as a deploy-ready smart-contract project.

Confirmed issues in the original source dump:

- The README was previously title-only.
- The active source dump is under `Maticaws/`.
- The main contract is `Maticaws/contracts/Maticaws.sol`.
- The repo contains partial vendored OpenZeppelin-style files.
- Some required dependency files in the source dump are empty.
- The import paths in the main contract do not match the vendored dependency layout.
- No complete Hardhat, Truffle, Foundry, or npm project setup was originally present.
- No tests were originally present.

## Confirmed original source layout

```text
Maticaws/
├── @openzeppelin/
│   └── contracts/
├── contracts/
│   └── Maticaws.sol
└── settings.json
```

## New repair scaffold

The repository now includes a Hardhat scaffold so the contract can be repaired, tested, and reviewed in a standard Solidity workflow.

```text
package.json
hardhat.config.js
docs/status.md
```

## Intended repair path

1. Preserve the original `Maticaws/` source dump.
2. Use OpenZeppelin Contracts 4.x through npm instead of relying on incomplete vendored files.
3. Move the repaired active contract into `contracts/Maticaws.sol`.
4. Add unit tests under `test/`.
5. Confirm compile success.
6. Fix mint logic, supply enforcement, reset-claim behavior, withdrawal behavior, and metadata behavior.
7. Run static analysis before any deployment.

## Original contract intent

The original contract appears to implement an NFT collection with:

- ERC-721 tokens.
- Enumerable token support.
- Token URI storage support.
- Pausing.
- Owner administration.
- Merkle-proof free mint rounds.
- Paid minting.
- A max supply of 6,996.
- A default metadata endpoint at `https://api.maticaws.club/metadata/`.

## Do not deploy as-is

The original source dump is not confirmed compile-ready and should not be deployed without repair, tests, and review.

## Recommended local workflow

```bash
npm install
npm run compile
npm test
```

## License

The original contract declares `MIT` in the Solidity source header. Add a dedicated `LICENSE` file if this repository is intended to remain public and reusable.
