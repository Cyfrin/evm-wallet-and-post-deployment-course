# Wallet & Post-Deployment Course

Welcome to the repository for the Wallet & Post-Deployment Security Course by Cyfrin Updraft!

This repository houses the written content of our courses, organized to facilitate easy access and contribution from our community.
Please refer to this for an in-depth explanation of the content:

-   [Website](https://updraft.cyfrin.io/) - Join Cyfrin Updraft and enjoy 50+ hours of smart contract development courses
-   [Twitter](https://twitter.com/cyfrinupdraft) - Stay updated with the latest course releases
-   [LinkedIn](https://www.linkedin.com/school/cyfrin-updraft/) - Add Updraft to your learning experiences
-   [Discord](http://discord.gg/cyfrin) - Join a community of 3000+ developers and auditors
-   [Newsletter](https://www.cyfrin.io/newsletter) - Weekly security research tips and resources to level up your career
-   [Codehawks](https://www.codehawks.com/) - Smart contracts auditing competitions to help securing web3


This was considered part 2 of the [security and auditing course](https://updraft.cyfrin.io/courses/security), but now, it's it's own living breathing course!

- [Wallet \& Post-Deployment Course](#wallet--post-deployment-course)
- [Introduction, Resources, and Prerequisites](#introduction-resources-and-prerequisites)
  - [Link to video: *Coming soon...*](#link-to-video-coming-soon)
  - [Resources For This Course](#resources-for-this-course)
    - [Challenge Contracts Registry](#challenge-contracts-registry)
  - [Potential Wallets](#potential-wallets)
    - [Browser](#browser)
    - [Hardware](#hardware)
    - [Multi-Sig](#multi-sig)
  - [Prerequisites](#prerequisites)
    - [Nice to have](#nice-to-have)
  - [Outcome](#outcome)
  - [Recommended Testnets](#recommended-testnets)
- [Section 1: Wallet \& Key Management](#section-1-wallet--key-management)
  - [Wallet types](#wallet-types)
    - [What to look for](#what-to-look-for)
  - [Wallet Safety](#wallet-safety)
  - [Cloud Wallet Infrastructure](#cloud-wallet-infrastructure)
  - [Verify Metamask transactions](#verify-metamask-transactions)
    - [Section 1 NFT](#section-1-nft)
- [Section 2: Post-deployment](#section-2-post-deployment)
  - [Summary of this whole section:](#summary-of-this-whole-section)
    - [For protocols](#for-protocols)
    - [For security researchers](#for-security-researchers)
  - [What to do, before you deploy](#what-to-do-before-you-deploy)
  - [Setup a security contact and policy](#setup-a-security-contact-and-policy)
  - [Monitoring](#monitoring)
  - [Incident Response](#incident-response)
  - [Bug Bounties](#bug-bounties)
  - [Responsible Disclosure / Finding bugs in production code](#responsible-disclosure--finding-bugs-in-production-code)
    - [What to do if you find a bug?](#what-to-do-if-you-find-a-bug)
    - [What if?](#what-if)
  - [Whitehatting](#whitehatting)
    - [Section 2 NFT](#section-2-nft)
- [Congratulations](#congratulations)
  - [Where do I go now?](#where-do-i-go-now)
  - [Learning More](#learning-more)
  - [Disclosures](#disclosures)
- [Thank you](#thank-you)
  - [Sponsors](#sponsors)
  - [Lead Lecturers / Code Builders](#lead-lecturers--code-builders)
  - [Guest Lecturers](#guest-lecturers)
  - [Special thanks](#special-thanks)
  - [Huge Extra Thank YOU](#huge-extra-thank-you)

# Introduction, Resources, and Prerequisites

## Link to video: *Coming soon...*

> ⚠️ All code associated with this course is for demo purposes only. They have been audited, but we do not recommend them for production use and should be used at your own risk. 

## Resources For This Course

Join [Cyfrin Updraft](https://updraft.cyfrin.io/) for the best learning experience!

- AI Frens
  - [ChatGPT](https://chat.openai.com/)
      - Just know that it will often get things wrong, but it's very fast!
  - [Phind](https://www.phind.com/)
      - Like ChatGPT, but it searches the web
  - [Gemini](https://gemini.google.com/)
  - [Other AI extensions](https://twitter.com/aisolopreneur/status/1654823630155464704?s=42&t=-pu_sCYtfrfPJU7OXfifrQ)
- Github Discussions 
    -   Ask questions and chat about the course here!
-   [Stack Exchange Ethereum](https://ethereum.stackexchange.com/)
    -   Great place for asking technical questions about Ethereum
-   [Peeranha](https://peeranha.io/)
    -   Decentralized Stack Exchange! 


### Challenge Contracts Registry

- [Challenge Contracts (Arbitrum)](https://arbiscan.io/address/0xDe0e797bfAd78F0615d75430C53F8fe3C9e49883#code)
- [Challenge Contracts (Sepolia)](https://sepolia.etherscan.io/address/0x31801c3e09708549c1b2c9e1cfbf001399a1b9fa#code)
- It's just numbers 9 -> 10
  - The rest are from the [security and auditing](https://updraft.cyfrin.io/courses/security) or the [assembly and formal verification](https://updraft.cyfrin.io/courses/formal-verification) course. 


## Potential Wallets 

*Note: We do not endorse any of the following wallets. All we have done is take a look to see if these wallets pass a small series of tests to make sure code that the developers release can be verified.*

### Browser
- [Metamask](https://metamask.io/)
- [Frame](https://frame.sh/) 
- [Rabby](https://github.com/RabbyHub/Rabby) 
- [Rainbow](https://rainbow.me/en-us/) 

### Hardware
- [Trezor](https://trezor.io/)
- [CypherRock](https://www.cypherock.com/)

### Multi-Sig
- [Safe](https://safe.global/)

## Prerequisites
An intermediate understanding of solidity. You don't need to be a pro, but you should be familiar with:

* Blockchain basics (transactions, blocks, decentralization, etc)
* Running a smart contract test suite (hardhat, foundry, truffle, etc)
* Solidity basics (variables, functions, structs, etc)

### Nice to have
- [Security & Auditing Course](https://updraft.cyfrin.io/courses/security)

## Outcome
* Understand the potential dangers of different wallets
* Understand how, as a protocol/developer, you should choose a wallet 
* Understand what you need in place after you deploy your contracts

## Recommended Testnets

- [See this link in the foundry full course, and use the same testnet](https://github.com/Cyfrin/foundry-full-course-f23?tab=readme-ov-file#testnet-faucets)

# Section 1: Wallet & Key Management

*Q: Why are we giving guidelines and not strict recommendations?*

A: The wallet industry is constantly changing, and takes a LOT of work to assess how good different wallets are. Additionally, if you know what to look out for, that is more valuable than us giving you point-in-time recommendations.

## Wallet types
- [Article](https://www.cyfrin.io/blog/what-should-i-use-to-store-my-cryptocurrency-web3-wallet-guide)
  - Custodial Wallets 
  - "Hot" Wallets
      - Metamask 
      - Frame 
      - Rabby 
      - Rainbow 
    - [Where is my private key stored?](https://support.metamask.io/hc/en-us/articles/360018766351-How-to-recover-your-Secret-Recovery-Phrase)
    - [Where does metamask store my seed?](https://ethereum.stackexchange.com/questions/52658/where-does-metamask-store-the-wallet-seed-file-path) 
  - "Cold" Wallets 
      - Cypherrock 
      - Trezor 
    - [Hacked hardware wallet](https://www.youtube.com/watch?v=dT9y-KQbqi4)
    - [Wallet Scrutiny Thread](https://github.com/Cyfrin/evm-wallet-and-post-deployment-course)
  - Multi-sig (Yes - Set one up) 
      - 1 of 1, or x of y 
      - Case Study: [Vulcan](https://rekt.news/vulcan-forged-rekt/) 
      - [Future: Account Abstraction](https://ethereum.org/en/roadmap/account-abstraction/) 
### What to look for
*Tl;dr - the same things you'd look for in a protocol!*
- Open source 
- Active development 
- Audit history (Who did the review? What did they find? How good is the group?) 
- non-custodial 
- Do they have a security bounty program 
- If they ask you to wear your wallet around your neck, stay far away from them 
- [Interview with Wallet Scrutiny](https://www.youtube.com/watch?v=tgUYxNiiras)
## Wallet Safety 
  - Store the private key, not the secret phrase
      - Paper wallet
      - "brain" wallet
      - Encrypted file
      - [Case Study: LastPass](https://krebsonsecurity.com/2023/09/experts-fear-crooks-are-cracking-keys-stolen-in-lastpass-breach/)
  - [Case Study: Mixin](https://rekt.news/mixin-rekt/)
  - Rotate keys
  - [Physical security](https://github.com/jlopp/physical-bitcoin-attacks/blob/master/README.md) 
  - Social recovery 
  - [Wallets](https://walletcompare.xyz/) 
## Cloud Wallet Infrastructure 
- [Case Study: Orbit](https://medium.com/orbit-chain/official-statement-regarding-orbit-bridge-exploit-551928f3dc52)
## Verify Metamask transactions 
  - Foundry's cast 
  - [Joinfire](https://app.joinfire.xyz/) 
  - Metamask snaps 

🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐

🔐 Exercises: 

1. [Set up your Safe!](https://safe.global/) 
2. Review classic key leeks
   1. `.env` leak with private keys
   2. Research one private key leak from [rekt.news](https://rekt.news/leaderboard/)
3. Check out [keepmesafe](https://github.com/Cyfrin/keepmesafe)

### Section 1 NFT 
- [Use your safe! (Arbitrum)](https://arbiscan.io/address/0x1C08AbbBFa26eBFb6aA014AC08803992802116D9)
- [Use your safe! (Sepolia)](https://sepolia.etherscan.io/address/0xaB67557218F60C06acA750B9F8A20018e5604ebf)

🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐🔐
<p align="right">(<a href="#table-of-contents">back to top</a>) ⬆️</p>

# Section 2: Post-deployment

*Ideally, you'll want all of this setup before you go to production.*

## Summary of this whole section: 
### For protocols 
1. Have a security contact / bug bounty / safe harbor before you deploy 
2. Setup monitoring before you deploy 
3. Run a disaster recovery drill before you deploy 

### For security researchers
1. **Never** exploit a smart contract without working with those responsible 
   1. Even if you have good intentions 
   2. The only caveat is **maybe** if the transaction is already in the mempool 
2. Get familiar with responsible disclosure 
3. Get familiar with toolings & platforms:
   1. Bug bounties
   2. Blockchain sleuthing 

[Watch this video from DeFi security summit](https://www.youtube.com/watch?feature=shared&v=jSpvDhuaCgc)

## What to do, before you deploy
1. Written & tested incident response plan
   1. Remember the [rekt-test](https://blog.trailofbits.com/2023/08/14/can-you-pass-the-rekt-test/)
   2. Have a "security contact" email in your code
      1. If you're a DAO, potentially elect a security officer
   3. Setup your monitoring system for invariants
   4. Setup your bug bounty/safe harbor program

## Setup a security contact and policy
- Example [Openzeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts/security)
  - Contact information 
  - Bug Bounty 
  - Security Patches / Disclosures / Advisories 
  - [Safe Harbor](https://github.com/security-alliance/safe-harbor)
  - Additional Audits 

## Monitoring 
  - Your own
  - [Forta](https://www.youtube.com/watch?v=42RcaQ8YTzQ)
  - [Pessimistic Spotter](https://spotter.pessimistic.io/#form)
  - [OZ Defender](https://defender.openzeppelin.com/#/sentinel)
  - [Gauntlet](https://www.gauntlet.xyz/)
  - [Chaos Labs](https://chaoslabs.xyz/)

## Incident Response 
- [SEAL](https://form.typeform.com/to/jJoH2ktE?typeform-source=securityalliance.org)
  - [SEAL Drills](https://securityalliance.notion.site/Live-Scenario-Documentation-520e7db48e2143f7bc41b729fb219996)
  - [Wargames](https://form.typeform.com/to/jJoH2ktE?typeform-source=securityalliance.org)
  - [Safe Harbor](https://github.com/security-alliance/safe-harbor)
  - [SEAL 911](https://t.me/seal_911_bot)

## Bug Bounties
  - Roll your own
  - Immunefi
  - HackerOne

## Responsible Disclosure / Finding bugs in production code
- [Watch this interview with Openzeppelin security expert](https://www.youtube.com/watch?v=KhmRoF1NynM)
### What to do if you find a bug? 
**Do not exploit it**
- [Responsible Disclosure](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html)
- Steps:
1. Contact the team / those resonsible / bug bounty program
   1. Optionally, if they have a bug bounty/responsible disclosure procedure, use that 
   2. SEAL 911 (or other 911 groups) is always a good option
2. "Close the windows and blinds"
   1. Make sure you're on a secure chat channel, for example an E2E encrypted [signal channel](https://signal.org/)
3. Verify the bug with the team / those responsible 
4. Come up with a game plan to fix 
   1. This is where things get hard. Potentially pause the protocol, try to sneak it past governance, etc. 
   2. Use a [MEV-proof RPC](https://www.youtube.com/watch?v=92bdU5uvsD8)
   3. Deploy and execute your fix in 1 single transaction, potentially with a [whitehat kit](https://github.com/emilianobonassi/whitehacks-kit) to batch your transactions together. 

### What if?
- They don't have a security contact or bug bounty
  - If there is really no one responsible for the code (this is web3 after all) you may have to announce and give people a long window of opportunity for them to leave the protocol, before announcing the issue. 
- They ignore the bug?
  - Give them a window to fix or acknowledge it, otherwise tell them you'll need to go public with the information. **Give people the chance to leave the protocol before you publically disclose the issue. Use this as a last resort!**
- They don't pay you for your work?
  - Difficult one. You can always blast them on Twitter, but that can backfire. Ideally everyone works together. 
  - If you start to negotiate a bounty, you are now a black hat. 
- The transaction is already in the mempool?
  - This is the only time it **might** be ok to exploit it, by front-running the attack. However, there still may be legal ramifications. 

## Whitehatting 
- Blockchain sleuthing
    - [Metadoc](https://blocksec.com/metadock)
    - [Phalcon](https://phalcon.xyz/)
    - [OpenChain](https://openchain.xyz/)
    - [Dune analytics](https://dune.com/browse/dashboards)
    - [Tenderly](https://tenderly.co/)
  - Up and coming
    - [GhostLogs](https://ghostlogs.xyz/)
    - [shadow.xyz](https://www.shadow.xyz/)

- White/No/Black Hat Case Studies 
    - Nohats
        - Balancer
        - Vyper
    - Whitehats
        - Astaria
        - ParaSpace 
    - Blackhats
        - Euler
        - Many more

🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠

🌠 Exercises: 
1. Write a post-mortem report on a hack or audit finding that you found interesting from [Solodit](https://solodit.xyz/).
   1. Once you do this, you should pass the URL of your blog to the Section 2 NFT
   2. You can use [Ciara's writeup as a template of what one should look like](https://www.cyfrin.io/blog/seneca-attack-hack-analysis-proof-of-concept)
   3. Then, post it on Twitter, and be sure to tag [@cyfrinupdraft](https://twitter.com/CyfrinUpdraft)!

### Section 2 NFT
- [Write a hack analysis! (Arbitrum)](https://arbiscan.io/address/0xf0e1F5bf6dbE3D46DBafBD68D4376E9985D57373#code)
- [Write a hack analysis! (Sepolia)](https://sepolia.etherscan.io/address/0x0b9B5Fa8D9f5dAC5d59b18230A27C36FBE670878)

🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠🌠

<p align="right">(<a href="#table-of-contents">back to top</a>) ⬆️</p>

# Congratulations

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed The Course! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

If you've made it this far... wow. 

## Where do I go now?

_Coming soon: The EVM, Assembly, and Formal Verification Course!!_

- Competititve Audits
  - [CodeHawks](https://codehawks.com)
    - We are working on many things to get you more deals. Stay tuned...
  - [Code4rena](https://code4rena.com/)
  - [Hats Finance](https://hats.finance/)
- [CodeHawks Discord](https://discord.gg/cyfrin)
- Start marketing your services
  - Twitter, Farcaster, LinkedIn, etc
  - Blogging: Medium, Mirror, etc
- Bug Bounties
  - [Immunefi](https://immunefi.com/)
  - [Hats Finance](https://hats.finance/)

## Learning More
- [Patrick Collins YouTube](https://www.youtube.com/c/patrickcollins)
- [Solodit](https://solodit.xyz/)
- [Block Threat Intelligence](https://newsletter.blockthreat.io?r=2mgsm7) (Referral Link)
- [Consensys Diligence Newsletter](https://consensys.io/diligence/newsletter/)
- [Owen Thurm YouTube](https://www.youtube.com/@0xOwenThurm)
- [The Red Guild YouTube](https://www.youtube.com/channel/UC7bn5DeABT6zQz-bn6GS1Yw)
- [Cyfrin YouTube](https://www.youtube.com/@CyfrinAudits)

## Disclosures

The Cyfrin team runs CodeHawks, Cyfrin Updraft, and private security reviews. They are an advisor to the Peeranha project, and run various blockchain nodes like Chainlink & Ethereum. Additionally, the are responsible for the creation of the Aderyn and Solodit tools.  

# Thank you

## Sponsors

- [Cyfrin](https://www.cyfrin.io/)
  - [Updraft](https://updraft.cyfrin.io/)
  - [CodeHawks](https://codehawks.com/)
  - [Solodit](https://solodit.xyz/)
- [Arbitrum Foundation](https://arbitrum.foundation/)
- [Certora](https://www.certora.com/)
- [Chainlink Labs](https://chainlinklabs.com/)

## Lead Lecturers / Code Builders

- [Patrick Collins | Cyfrin](https://twitter.com/PatrickAlphaC)

## Guest Lecturers

- XXXX

## Special thanks

- [hansfriese](https://twitter.com/hansfriese) 
- [carlitox477](https://twitter.com/carlitox477)
- [0Kage](https://twitter.com/hansfriese)
- [giovannidisiena.eth](https://twitter.com/giovannidisiena)
- [Dacian](https://twitter.com/DevDacian)
- [Alex Roan](https://twitter.com/alexroan)  

## Huge Extra Thank YOU

Thanks to everyone who is taking, participating in, and working on this course. These courses are passion project data dumps for everyone in the web3 ecosystem. 

Let's level up so we can keep web3 safer, and thank you again for taking this course!

[![Cyfrin Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/cyfrinaudits)
[![Cyfrin YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@CyfrinAudits)

<p align="right">(<a href="#table-of-contents">back to top</a>) ⬆️</p>

