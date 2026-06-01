<!--
****************************************************************************************
Title: README.md / Maticaws Source Code for CTO
Developed by: Ryan Hatch
Repository: ryanshatch/Maticaw-Source-Code-For-CTO
Project Type: ERC-721 CTO / Derug Source Review
Last Updated: June 1 2026
Version: 1.0.0
****************************************************************************************
-->

<hr>

<h1 align="center">Maticaws Source Code for CTO</h1>

<p align="center">
  <strong>ERC-721 Source Dump • CTO / Derug Review • Smart Contract Repair Scaffold</strong>
  <br>
  <strong>By: Ryan Hatch</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Project-Maticaws-0A2647?style=for-the-badge" alt="Project Name">
  <img src="https://img.shields.io/badge/Type-ERC--721%20NFT-144272?style=for-the-badge" alt="Project Type">
  <img src="https://img.shields.io/badge/Status-Review%20Material-205295?style=for-the-badge" alt="Project Status">
  <img src="https://img.shields.io/badge/CTO-Derug%20Source%20Review-2C74B3?style=for-the-badge" alt="CTO Review">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Solidity-%5E0.8.x-363636?style=for-the-badge&logo=solidity" alt="Solidity">
  <img src="https://img.shields.io/badge/Hardhat-Scaffolded-F7DF1E?style=for-the-badge&logo=hardhat" alt="Hardhat">
  <img src="https://img.shields.io/badge/OpenZeppelin-4.x-4E5EE4?style=for-the-badge" alt="OpenZeppelin">
  <img src="https://img.shields.io/badge/Deploy%20Status-Do%20Not%20Deploy%20As--Is-red?style=for-the-badge" alt="Do Not Deploy">
</p>

<hr>

<p align="center">
  <a href="#table-of-contents">Table of Contents</a><br>
  <a href="#project-status">Project Status</a> •
  <a href="#what-this-repository-is">What This Repository Is</a> •
  <a href="#original-contract-summary">Original Contract Summary</a> •
  <a href="#confirmed-repository-layout">Repository Layout</a> •
  <a href="#confirmed-issues">Confirmed Issues</a> •
  <a href="#repair-scaffold">Repair Scaffold</a> •
  <a href="#recommended-local-workflow">Local Workflow</a> •
  <a href="#repair-roadmap">Repair Roadmap</a> •
  <a href="#security-review-notes">Security Review</a> •
  <a href="#license">License</a> •
  <a href="#contact">Contact</a>
</p>

<hr>

<h2 id="table-of-contents" align="center">Table of Contents</h2>

<ol>
  <li><a href="#project-status">Project Status</a></li>
  <li><a href="#what-this-repository-is">What This Repository Is</a></li>
  <li><a href="#original-contract-summary">Original Contract Summary</a></li>
  <li><a href="#confirmed-repository-layout">Confirmed Repository Layout</a></li>
  <li><a href="#confirmed-issues">Confirmed Issues</a></li>
  <li><a href="#repair-scaffold">Repair Scaffold</a></li>
  <li><a href="#recommended-local-workflow">Recommended Local Workflow</a></li>
  <li><a href="#smart-contract-behavior">Smart Contract Behavior</a></li>
  <li><a href="#minting-system">Minting System</a></li>
  <li><a href="#free-mint-and-merkle-system">Free Mint and Merkle System</a></li>
  <li><a href="#admin-controls">Admin Controls</a></li>
  <li><a href="#known-risk-areas">Known Risk Areas</a></li>
  <li><a href="#repair-roadmap">Repair Roadmap</a></li>
  <li><a href="#recommended-tests">Recommended Tests</a></li>
  <li><a href="#security-review-notes">Security Review Notes</a></li>
  <li><a href="#do-not-deploy-as-is">Do Not Deploy As-Is</a></li>
  <li><a href="#future-improvements">Future Improvements</a></li>
  <li><a href="#license">License</a></li>
  <li><a href="#contact">Contact</a></li>
</ol>

<hr>

<h2 id="project-status" align="center">Project Status</h2>

<p>
  <strong>This repository is currently review material.</strong>
</p>

<p>
  It contains a preserved <strong>Maticaws ERC-721 source-code dump</strong> for CTO / derug review.
  The original source should not be treated as deploy-ready until the contract compiles cleanly, dependency issues are fixed, tests are added, and the mint logic is reviewed.
</p>

<blockquote>
  <strong>Status:</strong> Preserved source dump with repair scaffold. Not confirmed production-ready. Do not deploy as-is.
</blockquote>

<table>
  <thead>
    <tr>
      <th align="left">Area</th>
      <th align="left">Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Original source dump</td>
      <td>Preserved under <code>Maticaws/</code></td>
    </tr>
    <tr>
      <td>Main original contract</td>
      <td><code>Maticaws/contracts/Maticaws.sol</code></td>
    </tr>
    <tr>
      <td>README</td>
      <td>Expanded from title-only documentation</td>
    </tr>
    <tr>
      <td>Hardhat scaffold</td>
      <td>Added for repair workflow</td>
    </tr>
    <tr>
      <td>Tests</td>
      <td>Not yet implemented</td>
    </tr>
    <tr>
      <td>Compile status</td>
      <td>Not confirmed</td>
    </tr>
    <tr>
      <td>Deploy status</td>
      <td>Do not deploy as-is</td>
    </tr>
  </tbody>
</table>

<hr>

<h2 id="what-this-repository-is" align="center">What This Repository Is</h2>

<p>
  <strong>Maticaws Source Code for CTO</strong> is a preservation and repair workspace for a Maticaws NFT smart contract source dump.
</p>

<p>
  The goal is not to immediately redeploy the contract. The goal is to:
</p>

<ul>
  <li>Preserve the original source material.</li>
  <li>Document what the original contract appears to do.</li>
  <li>Identify compile and dependency issues.</li>
  <li>Create a proper Hardhat repair workflow.</li>
  <li>Prepare the contract for testing, review, and possible CTO / derug use.</li>
</ul>

<p>
  The original commit history indicates the repo was added for potential derug / CTO review. This repository should therefore be treated as a source archive and repair project first.
</p>

<hr>

<h2 id="original-contract-summary" align="center">Original Contract Summary</h2>

<p>
  The original contract is named <code>Maticaws</code>.
</p>

<table>
  <thead>
    <tr>
      <th align="left">Property</th>
      <th align="left">Confirmed Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Contract name</td>
      <td><code>Maticaws</code></td>
    </tr>
    <tr>
      <td>Token name</td>
      <td><code>Maticaws</code></td>
    </tr>
    <tr>
      <td>Token symbol</td>
      <td><code>MATICAW</code></td>
    </tr>
    <tr>
      <td>Token standard</td>
      <td>ERC-721</td>
    </tr>
    <tr>
      <td>Max supply</td>
      <td><code>6996</code></td>
    </tr>
    <tr>
      <td>Original mint price</td>
      <td><code>15 ether</code></td>
    </tr>
    <tr>
      <td>Max mint per transaction</td>
      <td><code>100</code></td>
    </tr>
    <tr>
      <td>Metadata base URI</td>
      <td><code>https://api.maticaws.club/metadata/</code></td>
    </tr>
    <tr>
      <td>Solidity pragma</td>
      <td><code>^0.8.9</code></td>
    </tr>
  </tbody>
</table>

<p>
  The original contract imports OpenZeppelin ERC-721, enumerable token support, URI storage, pausing, ownership, counters, and Merkle proof utilities.
</p>

<hr>

<h2 id="confirmed-repository-layout" align="center">Confirmed Repository Layout</h2>

<p>
  The original source dump is preserved under <code>Maticaws/</code>.
</p>

<pre><code class="language-text">Maticaw-Source-Code-For-CTO/
├── README.md
├── package.json
├── hardhat.config.js
├── .gitignore
├── docs/
│   ├── status.md
│   └── repair-checklist.md
└── Maticaws/
    ├── @openzeppelin/
    │   └── contracts/
    ├── contracts/
    │   └── Maticaws.sol
    └── settings.json
</code></pre>

<p>
  The <code>Maticaws/</code> folder should be kept as original source material unless a deliberate archive strategy is chosen.
</p>

<hr>

<h2 id="confirmed-issues" align="center">Confirmed Issues</h2>

<p>
  The original source dump has several confirmed or strongly suspected problems that must be addressed before deployment.
</p>

<h3>1. Incomplete OpenZeppelin dependency files</h3>

<p>
  The vendored OpenZeppelin copy appears incomplete. Some expected dependency files are empty, including:
</p>

<ul>
  <li><code>Maticaws/@openzeppelin/contracts/access/Ownable.sol</code></li>
  <li><code>Maticaws/@openzeppelin/contracts/security/Pausable.sol</code></li>
</ul>

<p>
  These are required by the main contract. If the local vendored files are used, the project will not compile correctly.
</p>

<h3>2. Import path mismatch</h3>

<p>
  The main contract imports OpenZeppelin using the normal npm package layout:
</p>

<pre><code class="language-solidity">import "@openzeppelin/contracts/token/ERC721/ERC721.sol";
import "@openzeppelin/contracts/token/ERC721/extensions/ERC721Enumerable.sol";
import "@openzeppelin/contracts/token/ERC721/extensions/ERC721URIStorage.sol";
</code></pre>

<p>
  The preserved vendored layout does not fully match those paths. This should be fixed by using OpenZeppelin from npm instead of relying on the incomplete local copy.
</p>

<h3>3. Missing original project tooling</h3>

<p>
  The original source dump did not include a complete Hardhat, Truffle, Foundry, or npm project setup.
</p>

<h3>4. Missing tests</h3>

<p>
  No original unit tests were confirmed.
</p>

<h3>5. Free-mint reset logic needs review</h3>

<p>
  The original reset-claim logic appears weak because the reset-round check compares the existing claimed amount against the requested amount.
  This may allow repeated claims in reset mode depending on the Merkle proof and claim amount.
</p>

<h3>6. Owner mint can bypass max supply</h3>

<p>
  The original owner-only <code>safeMint</code> function does not appear to check <code>MAX_SUPPLY</code> before minting.
</p>

<h3>7. BOGO mint accounting should be cleaned up</h3>

<p>
  The original BOGO logic mints the paid amount first, then checks the free amount later.
  A safer approach is to calculate the total mint amount before minting anything.
</p>

<h3>8. Withdraw uses <code>transfer</code></h3>

<p>
  The original withdraw function uses <code>transfer</code>. A modern repair should consider the <code>call</code> pattern for better compatibility with contract-owner wallets.
</p>

<hr>

<h2 id="repair-scaffold" align="center">Repair Scaffold</h2>

<p>
  A Hardhat scaffold has been added to make the repair process easier.
</p>

<h3>Confirmed scaffold files</h3>

<pre><code class="language-text">package.json
hardhat.config.js
.gitignore
docs/status.md
docs/repair-checklist.md
</code></pre>

<h3>Package scripts</h3>

<pre><code class="language-json">{
  "scripts": {
    "compile": "hardhat compile",
    "test": "hardhat test",
    "clean": "hardhat clean"
  }
}
</code></pre>

<h3>Dependency direction</h3>

<p>
  The repair scaffold is intended to use:
</p>

<ul>
  <li><code>hardhat</code></li>
  <li><code>@nomicfoundation/hardhat-toolbox</code></li>
  <li><code>@openzeppelin/contracts@4.8.3</code></li>
</ul>

<p>
  OpenZeppelin 4.x is the intended target because the original contract uses OpenZeppelin 4-style inheritance and override patterns.
</p>

<hr>

<h2 id="recommended-local-workflow" align="center">Recommended Local Workflow</h2>

<p>
  After cloning the repository, install dependencies:
</p>

<pre><code class="language-bash">npm install</code></pre>

<p>
  Compile the active contract:
</p>

<pre><code class="language-bash">npm run compile</code></pre>

<p>
  Run tests:
</p>

<pre><code class="language-bash">npm test</code></pre>

<p>
  Clean Hardhat artifacts:
</p>

<pre><code class="language-bash">npm run clean</code></pre>

<blockquote>
  <strong>Important:</strong> The active repaired contract still needs to be added under <code>contracts/Maticaws.sol</code> before compile and test commands can fully validate the project.
</blockquote>

<hr>

<h2 id="smart-contract-behavior" align="center">Smart Contract Behavior</h2>

<p>
  The original <code>Maticaws</code> contract appears to support:
</p>

<ul>
  <li>ERC-721 minting.</li>
  <li>Enumerable token tracking.</li>
  <li>Token URI storage.</li>
  <li>Pausable transfers and minting hooks.</li>
  <li>Owner-only administration.</li>
  <li>Paid minting.</li>
  <li>Merkle-proof free minting.</li>
  <li>Three free-mint rounds.</li>
  <li>Round reset flags.</li>
  <li>Buy-one-get-one-free mode.</li>
  <li>Owner withdrawal.</li>
  <li>Owner base URI updates.</li>
  <li>Owner Merkle root updates.</li>
</ul>

<hr>

<h2 id="minting-system" align="center">Minting System</h2>

<h3>Paid minting</h3>

<p>
  The original paid mint function accepts an <code>amount</code>, checks max mint per transaction, checks max supply, verifies payment, and mints the requested amount.
</p>

<p>
  Original mint economics:
</p>

<ul>
  <li><code>PRICE_PER_MINT = 15 ether</code></li>
  <li><code>MAX_MINT_PER_TX = 100</code></li>
  <li><code>MAX_SUPPLY = 6996</code></li>
</ul>

<h3>BOGO mode</h3>

<p>
  The original contract includes a <code>b1g1f</code> flag.
  When enabled, the contract attempts to mint a second batch equal to the requested amount.
</p>

<p>
  Intended behavior appears to be:
</p>

<pre><code class="language-text">BOGO off:
pay for 1 -> receive 1

BOGO on:
pay for 1 -> receive 2
</code></pre>

<p>
  This should be tested and repaired before deployment.
</p>

<hr>

<h2 id="free-mint-and-merkle-system" align="center">Free Mint and Merkle System</h2>

<p>
  The original contract uses Merkle proof verification for free mints.
</p>

<p>
  The proof node is created with:
</p>

<pre><code class="language-solidity">keccak256(abi.encodePacked(msg.sender, amount))</code></pre>

<p>
  This means the allowlist proof appears tied to:
</p>

<ul>
  <li>the claimant wallet address, and</li>
  <li>the allowed mint amount.</li>
</ul>

<h3>Original free-mint rounds</h3>

<p>
  The contract defines three free-mint rounds:
</p>

<ul>
  <li><code>Round1</code></li>
  <li><code>Round2</code></li>
  <li><code>Round3</code></li>
</ul>

<p>
  It also defines <code>NoFreeMints</code> for supply windows where free minting is disabled.
</p>

<h3>Original round windows</h3>

<pre><code class="language-text">Supply <= 501       -> Round1
Supply <= 2000      -> NoFreeMints
Supply <= 2500      -> Round2
Supply <= 5001      -> NoFreeMints
Supply <= 5500      -> Round3
Supply > 5500       -> NoFreeMints
</code></pre>

<p>
  These boundaries should be reviewed because token IDs appear to start at <code>0</code>.
</p>

<hr>

<h2 id="admin-controls" align="center">Admin Controls</h2>

<p>
  The original contract includes owner-only controls for:
</p>

<ul>
  <li>Withdrawing contract balance.</li>
  <li>Setting the base URI.</li>
  <li>Setting mint price.</li>
  <li>Setting max mint per transaction.</li>
  <li>Setting the Merkle root.</li>
  <li>Turning BOGO mode on or off.</li>
  <li>Setting round reset flags.</li>
  <li>Pausing the contract.</li>
  <li>Unpausing the contract.</li>
  <li>Owner minting with a custom URI.</li>
</ul>

<p>
  These controls are normal for an NFT contract during development and launch, but they must be clearly documented before any CTO use.
</p>

<hr>

<h2 id="known-risk-areas" align="center">Known Risk Areas</h2>

<table>
  <thead>
    <tr>
      <th align="left">Risk Area</th>
      <th align="left">Why It Matters</th>
      <th align="left">Recommended Fix</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Incomplete dependencies</td>
      <td>Contract may not compile</td>
      <td>Use npm OpenZeppelin 4.x</td>
    </tr>
    <tr>
      <td>Import mismatch</td>
      <td>Build path may fail</td>
      <td>Move repaired contract to <code>contracts/</code></td>
    </tr>
    <tr>
      <td>Free-mint reset logic</td>
      <td>May allow repeated claims</td>
      <td>Use reset epochs</td>
    </tr>
    <tr>
      <td>Owner safe mint</td>
      <td>May exceed max supply</td>
      <td>Add max supply check</td>
    </tr>
    <tr>
      <td>BOGO logic</td>
      <td>Supply checks happen in two stages</td>
      <td>Calculate total mint amount first</td>
    </tr>
    <tr>
      <td>Withdraw via transfer</td>
      <td>May fail with contract owners</td>
      <td>Use <code>call</code> pattern</td>
    </tr>
    <tr>
      <td>No tests</td>
      <td>Behavior is not verified</td>
      <td>Add Hardhat tests</td>
    </tr>
    <tr>
      <td>Metadata assumptions</td>
      <td>Base URI may be stale</td>
      <td>Verify metadata endpoint</td>
    </tr>
  </tbody>
</table>

<hr>

<h2 id="repair-roadmap" align="center">Repair Roadmap</h2>

<h3>Phase 1: Preserve</h3>

<ul>
  <li>Keep the original <code>Maticaws/</code> folder intact.</li>
  <li>Use it as archive/source-reference material.</li>
  <li>Do not overwrite the original dump until a clean version is validated.</li>
</ul>

<h3>Phase 2: Build Scaffold</h3>

<ul>
  <li>Add Hardhat setup.</li>
  <li>Add npm package scripts.</li>
  <li>Add OpenZeppelin 4.x dependency.</li>
  <li>Add clean source and test paths.</li>
</ul>

<h3>Phase 3: Repaired Active Contract</h3>

<ul>
  <li>Add repaired source at <code>contracts/Maticaws.sol</code>.</li>
  <li>Use npm OpenZeppelin imports.</li>
  <li>Remove reliance on incomplete vendored OpenZeppelin files.</li>
  <li>Keep original source dump unchanged.</li>
</ul>

<h3>Phase 4: Logic Repairs</h3>

<ul>
  <li>Add max supply check to owner minting.</li>
  <li>Fix free-mint reset tracking with epochs.</li>
  <li>Calculate BOGO total mint amount before minting.</li>
  <li>Add reentrancy protection to mint and withdraw flows.</li>
  <li>Review exact payment versus overpayment.</li>
  <li>Review token ID start point.</li>
  <li>Review free-mint round boundaries.</li>
</ul>

<h3>Phase 5: Testing</h3>

<ul>
  <li>Add constructor tests.</li>
  <li>Add paid mint tests.</li>
  <li>Add BOGO tests.</li>
  <li>Add free-mint Merkle proof tests.</li>
  <li>Add pause/unpause tests.</li>
  <li>Add owner-only permission tests.</li>
  <li>Add max supply tests.</li>
  <li>Add withdrawal tests.</li>
</ul>

<h3>Phase 6: Review</h3>

<ul>
  <li>Run Hardhat compile.</li>
  <li>Run Hardhat tests.</li>
  <li>Run static analysis.</li>
  <li>Review deployed metadata assumptions.</li>
  <li>Confirm collection economics before any testnet or mainnet deployment.</li>
</ul>

<hr>

<h2 id="recommended-tests" align="center">Recommended Tests</h2>

<h3>Constructor Tests</h3>

<ul>
  <li>Confirms token name is <code>Maticaws</code>.</li>
  <li>Confirms token symbol is <code>MATICAW</code>.</li>
  <li>Confirms initial Merkle root is stored.</li>
  <li>Confirms initial base URI behavior.</li>
</ul>

<h3>Paid Mint Tests</h3>

<ul>
  <li>Allows mint with exact required payment.</li>
  <li>Rejects mint with insufficient payment.</li>
  <li>Rejects amount greater than max mint per transaction.</li>
  <li>Rejects mint that exceeds max supply.</li>
  <li>Correctly increments total supply.</li>
</ul>

<h3>BOGO Tests</h3>

<ul>
  <li>When disabled, minting <code>1</code> gives <code>1</code>.</li>
  <li>When enabled, minting <code>1</code> gives <code>2</code>.</li>
  <li>Rejects BOGO mints that exceed max transaction amount.</li>
  <li>Rejects BOGO mints that exceed max supply.</li>
</ul>

<h3>Free Mint Tests</h3>

<ul>
  <li>Valid Merkle proof allows claim.</li>
  <li>Invalid Merkle proof fails.</li>
  <li>Claim outside free-mint round fails.</li>
  <li>Same wallet cannot claim same round twice.</li>
  <li>Reset mode behaves exactly as intended.</li>
</ul>

<h3>Admin Tests</h3>

<ul>
  <li>Only owner can set price.</li>
  <li>Only owner can set max mint amount.</li>
  <li>Only owner can set Merkle root.</li>
  <li>Only owner can pause and unpause.</li>
  <li>Only owner can withdraw.</li>
  <li>Owner mint respects max supply.</li>
</ul>

<hr>

<h2 id="security-review-notes" align="center">Security Review Notes</h2>

<p>
  Before this contract is used in any CTO or derug situation, review these areas carefully:
</p>

<ul>
  <li><strong>Access control:</strong> Confirm owner privileges are acceptable.</li>
  <li><strong>Supply cap:</strong> Confirm no path can exceed <code>MAX_SUPPLY</code>.</li>
  <li><strong>Merkle claims:</strong> Confirm claim replay is impossible.</li>
  <li><strong>Payment handling:</strong> Decide whether exact payment is required.</li>
  <li><strong>BOGO behavior:</strong> Confirm economics are intentional.</li>
  <li><strong>Metadata:</strong> Confirm URI behavior and endpoint availability.</li>
  <li><strong>Pause behavior:</strong> Confirm pausing transfers is intended.</li>
  <li><strong>Withdraw behavior:</strong> Confirm owner wallet compatibility.</li>
  <li><strong>Token IDs:</strong> Confirm whether token IDs should start at <code>0</code> or <code>1</code>.</li>
</ul>

<hr>

<h2 id="do-not-deploy-as-is" align="center">Do Not Deploy As-Is</h2>

<p>
  This repository should not be deployed directly from the original source dump.
</p>

<p>
  The original source is useful as review material, but deployment should wait until:
</p>

<ol>
  <li>The repaired active contract is added under <code>contracts/</code>.</li>
  <li>The project compiles with npm OpenZeppelin 4.x.</li>
  <li>Unit tests pass.</li>
  <li>Static analysis is complete.</li>
  <li>Metadata behavior is confirmed.</li>
  <li>Ownership and CTO assumptions are documented.</li>
</ol>

<hr>

<h2 id="future-improvements" align="center">Future Improvements</h2>

<ul>
  <li>Add repaired <code>contracts/Maticaws.sol</code>.</li>
  <li>Add <code>test/Maticaws.test.js</code>.</li>
  <li>Add <code>scripts/deploy.js</code>.</li>
  <li>Add <code>.env.example</code>.</li>
  <li>Add <code>LICENSE</code>.</li>
  <li>Add Slither or other static analysis notes.</li>
  <li>Add a deployment checklist.</li>
  <li>Add a CTO handoff checklist.</li>
  <li>Add metadata endpoint validation notes.</li>
  <li>Add contract verification instructions for block explorers.</li>
</ul>

<hr>

<h2 id="license" align="center">License</h2>

<p>
  The original Solidity contract declares:
</p>

<pre><code class="language-solidity">// SPDX-License-Identifier: MIT</code></pre>

<p>
  A dedicated <code>LICENSE</code> file should be added if this repository is intended to remain public and reusable.
</p>

<p>
  Until a dedicated license file is added, treat the license status as partially documented by the Solidity source header only.
</p>

<hr>

<h2 id="contact" align="center">Contact</h2>

<p align="center">
  Maintained by <strong>Ryan Hatch</strong>.
</p>

<p align="center">
  <a href="https://github.com/ryanshatch">GitHub: ryanshatch</a>
</p>

<hr>

<p align="center">
  <strong>Maticaws Source Code for CTO</strong>
  <br>
  <em>Preserve the source, repair the contract, test before trust.</em>
</p>