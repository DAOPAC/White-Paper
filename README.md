# DAOPAC

💡 Join the Discord: 📜 [https://discord.gg/VvtJfTZrr7](https://discord.gg/VvtJfTZrr7) 📜

💡 Help is needed!
-  👩🏼‍💻 Rust developers for Solana blockchain dev 
- 🤓 Policy wonks for campaign ideas and solicitation
- 💰 Donors to set DAOPAC up with resources

<hr/>
<br>

> To all the worrywarts out there who said super PACs were going to lead to a cabal of billionaires secretly buying democracy: wrong! They are publicly buying democracy. 
— Stephen Colbert
> 

This decentralized political action committee (dPAC) is our response to the dark money allowed to flood into American politics after the Supreme Court’s 2010 ruling in *Citizens United v. Federal Election Commission*.

Making small contributions to political campaigns and nonprofits has not prevented powerful lobbies from continuing to subvert the will of the people. It is time for us to join forces and do something about it. The purpose of this organization is to safely and securely pool funds to influence politicians and win their votes. 

We are the people's PAC, controlled by code, driven by democracy, with the goal of winning the political game.

# Mission and Vision

Our mission is to provide a counterweight to the dark money rampantly flowing into our political system by publicly pooling money from the people in order to win political fights for the common good. 

Our vision is for the laws of the United States of America to accurately reflect the will of the people.

# Addressable Market

Charity is a massive market. Americans donate roughly 2% of GDP, or over $400 billion dollars, according to [GivingUSA](https://givingusa.org/giving-usa-2020-charitable-giving-showed-solid-growth-climbing-to-449-64-billion-in-2019-one-of-the-highest-years-for-giving-on-record/). Of that amount, about 70% comes from individual donors. The remainder is given by foundations and corporations. Our market is the charitable giving market. 

# Problem

Large donors receive disproportionate attention from recipients even though individual contributors make up the vast majority of total donations. This is an efficiency problem; it's much easier for the recipients to court one large check rather than many small checks. 

As a result, individual donors are not able to influence recipients to take the actions that they want them to take. Furthermore, donating to political candidates is risky as donations to losing campaigns may never be deployed on the trail and lack of visibility into spending details is frustrating. 

# Solution

DAOPAC will build three new political fundraising tools:

1. A sophisticated, purpose-built decentralized autonomous organization (DAO) to manage political funding decisions, and 
2. A smart contract-based process for conditional funding based on political events
3. A set of political event Oracles to trigger smart contract-based Campaigns (defined below)

Some political donation decisions are not binary. Is the candidate or incumbent doing "enough" to fight climate change? Tracking the introduction of bills or voting history is too complex for a simple conditional trigger. Decisions will require a nuanced debate. For this case, we created a DAO to facilitate the decision-making process. 

A DAO is a set of rules that govern how an organization operates. To maintain consistency and transparency, these rules are codified in a programming language and deployed to an immutable blockchain. All of our funding decisions will be made through the DAO.

Other decisions can be binary. We can fund every politician who votes in favor of a specified bill or pre-defined list of bills. We can fund every politician who scores 100% on the [League of Conservation Voters Scorecard](https://scorecard.lcv.org/members-of-congress). We can fund a candidate now and commit to funding again if they win their primary. These smart contracts would be publicly available so anyone can participate, not just the DAO. 

These new smart contracts allow for interesting fundraising possibilities:

- A politician can run two campaigns on the same bill, one for a YES vote and one for a NO vote, leading up to a controversial vote. They may choose to vote for the campaign that has the most money.
- A candidate can run a campaign with a matching donation from a blockchain wallet up to a specified amount, codifying the common "double your gift" fundraising tactic with a smart contract.
- A candidate can run a general campaign during the primary, gathering donations that will be released only if they win the primary, in order to prove momentum.
- An advocacy group can run a campaign for all candidates who perform on their voting scorecard, automatically distributing funds evenly among those candidates who meet the criteria.

All of the above campaigns would be fully transparent with smart contract logic written into a public blockchain and wallet values publicly accessible. Oracles that trigger these campaigns will be created by third parties and audited by the DAO or created by the DAO itself. Donors will have full awareness of the rules and outcomes.

Transparency will be put into a process that has been hidden from public.

# Structure

DAOPAC is not aligned with a particular political party or agenda. Instead, it is focused on a slate of issues that is defined at regular intervals by its structure:

![DAOPAC Structure](https://github.com/DAOPAC/White-Paper/blob/main/structure.png?raw=true)
[Link to Whimsical](https://whimsical.com/daopac-funding-BkYVrQQGmVRaVi5HwCYvtj)

## Directors

Directors are responsible for the DAO's operations. Tasks may include:

- Nurturing the broader community by participating actively in Discord and other media
- Responding to threads on DAO repository issues and pull requests
- Representing the DAO in a positive way to the public
- Coordinating with [Donors](#donors) to introduce new Proposals
- Auditing [Campaigns](#campaigns) and their identities
- Working with partners, especially political event [Oracles](#oracles)

For this work, Directors receive a Carry a configurable quantity of locked [Tokens](#tokens) each month, distributed evenly among all of the Directors.

## Donors

Donors are people who have either purchased or earned our [Token](#tokens). [Tokens](#tokens) are purchased directly through the DAOPAC website or, eventually, through a token exchange. 

To earn tokens, Donors can complete a short course about new campaigns similar to the [Coinbase Earn](https://www.coinbase.com/earn) program. 

In order to use tokens for voting, Donors must complete an identity protocol for FEC compliance. Voting will either be handled through the DAOPAC website or through a DAO management platform.

No Donor will be able to own more than a configurable percentage of the [Token](#tokens) supply.

At any time, a Donor may sell their tokens and leave DAOPAC. 

## Campaigns

A Campaign is either a wallet or a smart contract. 

A wallet is a blockchain address that holds cryptocurrencies.  You can think of a wallet Campaign as unconditional because the value goes straight to wallet if the DAO approves a Proposal to fund a Campaign. 

A smart contract Campaign, by contrast, is conditional in that it can allow for funding only if pre-specified conditions are met. A smart contract Campaign may be conditioned on an election or the release of a voting scorecard score. A smart contract campaign will, by necessity, depend on a trusted data source (see [Oracles](#oracles) below) to confirm that the event took place. These Campaigns can be written to automatically refund if the condition is not met. 

Anyone will be able to donate to a Campaign, not just the DAO.

## Proposals

A Proposal is composed of five elements: a Campaign, a Donor, a Director, an Amount, and a Time. These elements are defined as follows:

- Campaign: a wallet address or a smart contract address to be funded by the DAO (address)
- Donor: the wallet address of the Donor responsible for the Proposal (address)
- Directors: the wallet address of the Director who approved the Proposal (address)
- Amount: an amount of cryptocurrency to be transferred to the Campaign (unsigned float)
- Time: the date and time for the start of the Vote (timestamp)

If a Director comes up with a Proposal alone, they still must identify a lead Donor to be affiliated with and advocate for the Proposal. A Donor must likewise identify a Director to sponsor and review the Proposal before introducing it to DAOPAC.

## Voting

A Vote is the period beginning on a Proposal's Time and ending exactly 24 hours later. During this period Donors and Directors may vote for or against the Proposal.

A Proposal is approved if and only if it meets these two conditions:

1. A majority of voting tokens must be in favor
2. A majority of voting wallets must be in favor

This structure mimics the House of Representatives and the Senate as defined in the constitution of the United States of America. A majority of tokens must be in favor, as in the House, providing a weighted vote. Simultaneously, a majority of wallets must *also* be in favor, as in the Senate. A Donor abstains if they choose not to participate in the Vote and their wallet and tokens simply are not counted. 

If a Proposal is approved, the following will occur:

- the Amount of the Proposal will transfer from the DAO to the Campaign
- the Donor and Director of the Proposal will each receive a Bounty in $CHIT of X% of the Amount, where X is defined by the Director

# Oracles

The DAO may need to build its own Oracles in order to introduce new smart contract Campaigns that rely on certain political events. Other Oracles may be validated and trusted by third-parties such as Chainlink. 

Oracles must be audited and operating logic must be open-sourced. 

# Tokens

The DAO creates a supply of tokens (Ticker: $CHIT, the term for political favors) at genesis and allows for the exchange of $CHIT for $SOL (the Solana blockchain token) at an exchange rate that is set at genesis. The role of $CHIT is to allow Donors to opt out by finding other buyers (via a DEX, for example) to convert their $CHIT back to $SOL or any other currency. 

Without $CHIT, the DAO is like a joint bank account. When a Donor leaves, the value goes with them. We need $CHIT in order to create a stable supply of $SOL for DAOPAC funding.

The distribution of the genesis supply will be as follows:

- 5% to Genesis Term Directors
- 3% to Genesis Term advisors and partners
- 2% to future advisors and partners
- 20% to locked incentive pool
- 70% to donor pool

Additional $CHIT will be generated only with approval of a majority of Directors.

A multi-signature wallet will control the $SOL held in the DAO. The 

## Price Stability

To prevent Treasury and Campaign values from swinging wildly due to $SOL prices and the broader crypto ecosystem, the DAO will immediately swap SOL to a stablecoin like $USDC upon receipt of $SOL. 

Alternatively, the DAO may also decide to only accept stablecoins and put the burden on the Donor to acquire stablecoins first. 

Regardless, Campaigns will only accept stablecoins in order to protect against value volatility.

# Governance

## Genesis Term

During the Genesis Term, any Director can propose adding a new Director. New Directors are approved with at least 50% approval of the existing Directors. 

Directors cannot remove other Directors. 

The Directors during the Genesis Term are considered the Founders. 

The Genesis Term ends on January 1, 2023. 

Beyond the Genesis Term, DAOPAC's Founders hold no special privileges. 

## Terms

Terms begin on January 1, 2023 and last for one calendar year. 

## Pull Requests

Ownership of the DAOPAC Github repository is shared by some, but not necessarily all, of Directors. 

If a Director is demoted to a Donor during Change in Control, they may retain Github ownership if they are still actively maintaining the repository.

## Change in Control

Directors serve for a Term. Directors are able to remove themselves but there must always be at least two Directors. 

New Directors are chosen from the pool of Donors who have introduced Proposals during the Term. Each Donor is scored as follows:

- 2 point for each Proposal taken to a Vote during the Term
- 3 points for each Proposal approved during the Term
- 2 point for each approved Pull Request
- 1 point for each year involved in DAOPAC, measured daily

The Donors whose point totals are in the top quartile automatically become Directors for the next Term.

Directors who had zero points during the Term are automatically removed.

# Marketing

## Go-To-Market

The Genesis Term is critical for our go-to-market (GTM) strategy. 

## Crypto Politics

DAOPAC will work on political issues that are critical to the crypto community in the 2022 campaign cycle. Campaigns may include:

- The 1099-B requirement for cryptocurrency exchanges
- The Blockchain Regulatory Certainty Act which provides safe harbor for blockchain developers
- The Safe Harbor For Taxpayers With Forked Assets Act of 2021 which "delineates that receipt of a forked virtual currency may not constitute a taxable event"
- The Token Taxonomy Act which excludes tokens from being regulated
- The Digital Asset Market Structure and Investor Protection Act which gives the SEC authority over cryptocurrencies
- The Eliminate Barriers To Innovation Act of 2021 which attempts to define a security in the context of cryptocurrencies

Congress is only beginning to wrap their heads around these new financial and technological instruments. Now is prime time for the crypto community to become active in influencing the politics around crypto.

## Climate Politics

Because the climate crisis is so dire, and elected officials have been so inept, DAOPAC will also work on climate . 

According to [OpenSecrets](https://www.opensecrets.org/political-action-committees-pacs/industry-breakdown/2020), only $2.2M was deployed to candidates from environmental PACs in the 2020 cycle. By contrast, $7M was deployed to candidates from energy-related PACs.

Campaigns may include:

- Preserving the climate components of the Infrastructure Investment and Jobs Act
- Keep It in the Ground Act of 2021 to prohibit drilling in the outer Continental Shelf
- Methane Waste Prevention Act of 2021 to prevent methane waste and pollution from oil and gas operations
- Various state bills and elections, since a lot of climate change policy will be enacted locally

DAOPAC has the opportunity to be the largest environmental PAC in the world and finally and forcefully remove climate change-deniers and fossil fuel-friendly officials from office. This is a goal worth pursuing.

## Growth Strategies

Clever growth techniques will emerge as DAOPAC grows and brings more great people aboard. Initially, some interesting use cases are:

- NFTs can be created about each Campaign and used to fundraise for the Campaign
- NFTs can be automatically gifted to Donors who create successful Campaigns
- NFTs can be gifted to all DAOPAC Donors, similar to the "I VOTED" stickers on Election Day

# Roadmap
The following is a rough guide for how DAOPAC will unfold in 2022.

## Stage 0: Governance Formation (Nov '21 - Jan '22)

### Spec
This is the thinking part. There's a lot to consider when dealing with political entities, crypto markets, and donors. In order to move fast, we need prevent mistakes. This document is the result of that thinking. 

Getting a spec (or white paper or litepaper) developed and vetted past discerning people is an important step in the journey. So far, so good. The spec will continue to live and morph as we figure more stuff out. The team will need to keep this document updated as much as possible or, better yet, convert it into a Gitbook documentation system.

The technical spec has involved making several critical decisions. Among them are:

- Which blockchain will we use?
- Should we build our own DAO from scratch or use an existing library?
- What frontend framework should we use?
- Where will all of this be hosted?

These questions are mostly answered now. We'll build on Solana. We'll use the native [governance platform](https://realms.today/realms). Since most of the examples and packages are built for React, we'll use that frontend framework. Hosting can be anywhere, but Heroku or Vercel seem best. 

The tech spec will also evolve over time.
### Discord
The Discord is the gathering spot for information, ideas, and chatter about this project. It is alive and the link is at the top of the spec. Over time we'll add and archive channels and continue to invite more members. 

## Stage 1: Treasury Formation (Jan '22)
To use the Solana governance platform, we will need both a regular token and a council token. 

The keys for these tokens should be held in a multisig wallet. This way control over minting, burning, and freezing accounts isn't held be a single person. 

The token tickers and program IDs are shown here. 

### Token Mint
> CHIT: `Chitd6BnY9A1E46PkaH3q9q4u78AKMjiLVD85tWpz6sy`
### Council Mint
>DAOPAC: `DAoPaCBCFdCBM4NQ3c61h9HQwKqYi9V1VJQrPqaw1Hk6`

## Stage 2: Operationalization (Jan '22 - )
Here is an outline of what we can expect to accomplish throughout 2022.
### Q1 2022
- Go public with this paper and the Discord. Gather interest and organize it.
- Begin to work through legal complexities. 
- Set up GitHub repositories, Discord, social media. 
- Put together marketing and fundraising materials.
- **Goal: Deploy the conditional fundraising web3 dapp prototype.**

### Q2 2022
- Go live with first campaigns on the dapp. Build hype.
- Use the DAO to fundraise for dapp campaigns. 
- **Goal: 10 campaigns and $10 million**

### Q3 2022
- Demonstrate an impact on the 2022 midterms. Record data.

### Q4 2022
- Regroup and reassess. What worked? What can improve? 
- Look forward to 2024. Put a plan in place. 
