# Compound Asset Listing - Checklist

## Info that needs to be submitted by the proposer

*\* Indicates a required field*

### General

- [ ] Token Asset Name*
- [ ] A description of the project and the token*
- [ ] Benefits to Compound Community*
- [ ] Resources (Website, Social Media Links and docs)*
- [ ] The proposal author their contact info*
- [ ] The relationship between the author of the new market proposal and the token*
- [ ] Social channels Metrics (Size, activity and growth).

### Market Risk Assessment

- [ ] Market Cap of the token*
- [ ] The largest exchanges where the token is listed and its respective liquidity*
- [ ] Indicate the volatility of the token, defined as the Standard Deviation of log-returns for specific time frames by [Gauntlet](https://maker-report.gauntlet.network/int_vol).
- [ ] Total supply*
- [ ] Emission schedule.

### Decentralization

- [ ] How is this asset distributed amongst token holders? List the top 10 holders, the percentage of each holder, and tag any of them if they are known.*
- [ ] List all of the privileged roles in the token contract. This can include whitelisted EOAs, Multi-sigs or DAOs.*
- [ ] Is it pausable?*
- [ ] Does it have a blacklist?*

### Smart contract risks

#### Codebase & On-chain Activity:
- [ ] Provide a Github repository for the underlying token contracts*
- [ ] Provide a test suite with code coverage.
- [ ] Provide Etherscan links with verified contracts*
- [ ] Give the age of the token in days*
- [ ] Given the number of transactions in the contract to date*

#### Security Posture:
- [ ] What audits, if any, were performed? Provide links to the reports if they exist.*
- [ ] Does the project have an active bug bounty program?*
- [ ] Provide emergency contacts with their responsiveness levels and response availabilities* 
- [ ] List additional security and formal verification tools used in development
- [ ] List all monitoring services used by the token, if any.

#### Smart contract Behavoir:
- [ ] Does the token have more than one address[^1]?*
- [ ] Does the token use a compiler version greater than 0.8.0 or the SafeMath? If not, explain how the protocol deals with possible overflows and underflows*
- [ ] During the execution of the token's functions, does the token execute external code chosen by the caller or receiver?[^2] If so, please explain the reasoning behind this decision*
- [ ] How much does the token contract deviate from a standard implementation of ERC20? Any additional features that the Compound DAO should know about?*
- [ ] Is it burneable?*
- [ ] Does it have a fixed supply? If no, who can mint?*
- [ ] Is it a rebasing token?*
- [ ] Does the token charge fees on transfers?*
- [ ] Is the contract performing arbitrary `delegatecall`s?* If the answer is yes, indicate who can make these calls and to what contracts.
- [ ] Is it flash mintable? If yes, please provide more information on this feature*
- [ ] Is it flash loanable? If yes, please indicate who offers the service.*

#### Upgradability:
- [ ] Is it upgradeable?* If yes, answer the following questions:
  - [ ] Who is authorized to make an upgrade?
  - [ ] Can an upgrade happen instantaneously or is there a time-lock delay?
  - [ ] Which components are upgradable?
  - [ ] How does the upgradeability design work? Who manages it and are how upgrades performed?
  - [ ] Does it emit an event when the implementation is updated?
 
## Initial Requirements

- [ ] Set collateral factor to 0.
- [ ] Set established borrow limit if necessary (Usually it is set if large loans of this asset are associated with potential governance attacks related to the asset itself).
- [ ] Set reserve Factor to 25% (any other convenient value can be set in other proposals depending on the asset's volatility and category).

## Considerations

- [ ] Proposals must be first posted in the Compound forum *New Markets* category.
- [ ] The on-chain proposal must contain a link to the corresponding thread in the forum.
- [ ] One proposal per asset.
- [ ] All actions in the proposal must be related to the listing of the token.
- [ ] Do not deploy contracts without first submitting the proposal to the forum.
- [ ] Use markdown in the description of the proposal in the transaction, add links and start the title with # Add market: NAME.

## Community Check
The community should review the following items before approving a new asset.

- [ ] Veracity or the info provided.
- [ ] Correct configuration of the contracts (cToken, oracle, etc.).
- [ ] Documentation quality.
- [ ] Favorable results in the execution of the token test suite or integration simulations.

[^1]: [Double entry point vulnerability TUSD](https://blog.openzeppelin.com/compound-tusd-integration-issue-retrospective/).
[^2]: [C.R.E.A.M. Finance Post Mortem: AMP Exploit](https://medium.com/cream-finance/c-r-e-a-m-finance-post-mortem-amp-exploit-6ceb20a630c5).


