# W3F Grant Proposal

* **Project Name:** Kraken - a monorepo plugin for developing multiple Parity ink! smart contracts
* **Team Name:** Standard Protocol
* **USDC Payment Address:**  (PLEASE NOTE CHANGE)
* **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 2

## Project Overview :page_facing_up:

Inspired from squid spitting ink, I first tried to come up with the name "squid", but to glorify I named the framework "Kraken". Maybe name "squid" may be more memorable due to Squid Game, but I leave the decision to reviewers. 

In short, Kraken is monorepo parity ink! framework for versatile functions regarding wasm smart contract development on Polkadot ecosystem. The framework was initially being made for implementing Standard Protocol in ink!, but I see the opportunity to make it as offical smart contract dev tool.


### Overview

* Why Monorepo?

After developing wasm contract development framework [Houston](https://github.com/terra-money/houston) in Cosmos ecosystem. I found out it will never going to work like hardhat nor truffle because **Rust smart contracts are consisted of not just files, but projects**.
  1. They are wrapped in Cargo, which means you have to move around current working directory to compile each contract. (e.g. cd .. && cd ./contract1 && cargo build --release && ..)
  2. To import from other contracts, it is not done in path, you have to specify both path and version -> More tedious jobs
  3. Multiple compiled outputs in each project folder -> harder to locate each of them on deployment

To keep an eye on whole contracts, I found out the monorepo is the optimal way to develop them to provide the most same experience as existing solidity contract dev tools.

* Why Nx?

For cloud build.
![image](https://user-images.githubusercontent.com/12888144/177867044-74491815-860b-4e0e-ab36-95d021498699.png)

Rust smart contracts take extensive amount of time just to compile a contract.
Now imagine there are more than 10 of them, and you compile all of them. 
Cloud build was the necessary feature that we needed to work with.

* Reference?

I have tried working with other rust smart contract Cosmwasm.

[nxcw](https://github.com/digitalnativeinc/nxcw)

### Project Details

* [Standard Protocol Website](https://standard.tech/)

### Technologies
1. Rust
2. Parity ink!
3. Polkadot.js

### Components

### Nxink!

### 1. IP Sets & IP Files
* `Pallet_ips` - Provides basic functionality for creating and managing an `IPSet`. You can think of an `IPSet` as an idea, which is basically a collection of components (intellectual property tokens) that define and describe that idea.
* `Pallet_ipf` - Provides basic functionality for creating and managing an `IPToken`. You can think of an `IPToken` as a component of an idea. For example, a business summary PDF file, or even a 3D rendering of a prototype mold. When combined and stored in an `IPSet`, that collection forms the foundtion for an idea. The more detailed and/or comprehensive an `IPSet` is, the stronger the idea.

<div align=center>
  <img src="https://i.ibb.co/2q9ZJcP/IPL.png">
</div>

### 2. IP Licenses & Tokens
* `Pallet_dev` - Provides basic functionality for structuring, managing, and listing a `DEV`(Decentralized Entrepreneurial Venture). You can think of a `DEV` as an agreement between multiple parties to come together as cofounders over a project in order to contribute towards an `IPSet`'s actualization.
* `Pallet_dao` - Provides basic functionality for creating and managing a `DAO` that helps govern a `DEV`. You can think of a `DAO` as a `DEV`'s governance mechanism. It helps regulate the and ensure the integrity and prudence of participants within a `DEV`.
* `Pallet_worklog` - Provides basic functionality for creating and managing a `WorkLog` within a `DEV`. You can think of a `Worklog` as a `DEV`'s method of recording and storing milestone/deliverables progressions and completions.

<div align=center>
  <img src="https://i.ibb.co/4WCtTzh/055.png">
</div>

* Ownership can be fractionalized using multiple pegged fungible assets representing ownership (ARO). An ARO is (typically) reflected in the first IP Token (IPT) attached to an IP Set. The asset ID of an ARO is defined in a copyright ownership agreement, and there can be multiples of these fungible assets.

### Ecosystem Fit

:link:  **Chains and Pallets**<br>
InvArch applies the categories below:
* NFT
* Governance/DAO
* Other (IP Assets)

### Project Uniqueness
* The world's first truly composable network for fully unlocking IP assets & on-chain IP attribution solution (that is flexible for its assets to experience international compliance in business, copyright, & legal transactions. InvArch revolutionizes the world of innovation beginning at the very start of development & pushes the bounds of web3 by taking existing concepts & challenging them to be different and better. By unlocking new doors & redefining what’s possible, InvArch will revolutionize the worlds of technical development & real-world collaboration down to their very core.

### Target Audience
* Entrepreneurs/Innovators
* Developers/DAOs/Artists
* Educators/Researchers
* Philanthropists

### Problem Addressed
* On-chain IP attribution (Achieved with this grant proposal).
* International flexibility for compliance (Achieved with this grant proposal).
* Barriers of access to startup capital. (OCIF Protocol)
* On-chain donations for access & transparency. (OCIF Protocol)
* File piracy & inability to securely expose data. (XCA Protocol)

## Team :busts_in_silhouette:

### Team members 
(Development & Engineers)

* [Hyungsuk Kang](https://www.linkedin.com/in/hyungsukkang) - Founder & Head of Development

### Contact

* **Contact Name:** Hyungsuk Kang
* **Contact Email:** hyungsuk@standard.tech
* **Website:** [https://standard.tech](https://www.standard.tech)

### Legal Structure

Digital Native Foundation. </br> 
3 Fraser Street #05-25 Duo Tower, </br> 
Singapore </br> 

### Founders' experiences

* [Hyungsuk Kang](https://www.linkedin.com/in/hyungsukkang) has experience working in blockchain industry over 3 years and is a contributor to UST restitution group. He is now making a new standard in defi securing self-sovereignty of users' finance in web3.0 with enforceable financial contract.

### Team Code Repos

* Standard Protocol's team Github: https://github.com/digitalnativeinc

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

* [Hyungsuk Kang](https://www.github.com/hskang9) - Founder & Head of Development

### Team LinkedIn Profiles (if available)

* [Hyungsuk Kang](https://www.linkedin.com/in/hyungsukkang), Founder

## Development Status :open_book:

* 
## Development Roadmap :nut_and_bolt:

### Overview

* **Full-Time Equivalent (FTE):** 1
* **Total Costs:** $16000 equivalent

### Milestone 1 — Implement Nx plugin for Parity ink!

* **Estimated duration:** 4 weeks
* **FTE:**  1
* **Costs:** $14,000 equivalent USDC

Goal - Develop Nx plugin for boilerplate in Parity ink! contract project

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 |
| 0b. | Testing Guide | The code will have end-to-end test coverage to ensure functionality and robustness. In the guide we will describe how to run these tests. |
| 1. | Nx Plugin Repo | Complete the deployment of the InvArch chain (https://github.com/InvArch/InvArch) |

### Milestone 2 — Kraken CLI

* **Estimated duration:** 10 weeks
* **FTE:**  1
* **Costs:** $28,000 equivalent USDC

Goal - Make a CLI binary that can put this in a production level

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | GPLv3 | 
| 0b. | Documentation | Documentation on Github |
| 1. | Article & Video | 	We will write an **article** that explains the work done as part of the grant, as well as release a video walk through demonstrating Kraken |

## Future Plans

* Make indexer boilerplate with [SubQuery](https://linktr.ee/subquerynetwork)
* Test deployment in Canvas or Statemint common-good parachain.
* More example contract generators using XCM, Defi, NFT, etc
* Build Standard Protocol implementation in Parity ink!
* Maintain framework to adapt into multichain smart contract environment(e.g. support deploy command for deploying to other ink! contract chains)

## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?** 
I applied before.
