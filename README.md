<p align="center">
  <img src="assets/banner.jpg" alt="adiii.eth" width="100%">
</p>

<h1 align="center">adiii</h1>

<p align="center">
  <b>Smart Contract Engineer | Protocol Research</b><br>
  Onchain credit · Vaults · Tranching and credit risk · Fixed rate lending
</p>

<p align="center">
  <a href="https://x.com/0xPutAmaterasu">X</a> &nbsp;|&nbsp;
  <a href="https://adiii.eth.limo">adiii.eth.limo</a> &nbsp;|&nbsp;
  <a href="https://paragraph.com/@the-finance-sinner">Paragraph</a> &nbsp;|&nbsp;
  <a href="mailto:adiiiresearch@gmail.com">Email</a>
</p>

I build the financial layer that sits on top of onchain credit: the vaults that hold it, the tranches that decide who is paid first and who absorbs a loss, and the pricing and risk rules behind both. I was one of the founding engineers at Blok Capital, an onchain portfolio management protocol. I have shipped several onchain capital structures as early beta builds, and designed and built Morrow, the first risk product on top of Morpho Midnight, now in early beta. I believe every product should stand on a strong suite of financial modelling, formal verification and Foundry based testing before it ships.

<br>

## Experience

### Blok Capital &nbsp;|&nbsp; Founding Engineer

Core engineer on [Blok Capital](https://github.com/BLOKCapital)'s v1 protocol, a decentralized wealth management system of per user vaults built as EIP-2535 Diamonds and composed from a curated registry of protocol integration facets.

Built across the core protocol: integration facets for lending, fixed yield and perpetuals venues such as Morpho and Pendle, hardening of the Diamond facet surface, the offchain engine that computes and routes index rebalances, the first design of the multichain layer, and the token reward lock contracts with their unit, fuzz and invariant test suites. Alongside the engineering, researched the core protocol design end to end: how the vault architecture, facet registry, upgrade rules and integration surface fit together, and where the security boundaries sit.

Core contracts: [BLOKCapital/blokc-v1-core](https://github.com/BLOKCapital/blokc-v1-core)

<br>

## Featured: Morrow

**Dated senior and junior credit tranches on Morpho Midnight, behind two vault tokens.**

Morpho Midnight gave onchain credit fixed maturities. Morrow gives that credit a capital structure. One pool of fixed rate loans is split into a senior claim, paid first up to a fixed amount, and a junior claim that takes the first loss and keeps the residual. Lenders hold only srUSDC or jrUSDC, while capital runs through dated series that settle at maturity and roll automatically into the next.

Seniority cannot exist inside a Midnight market, where every lender shares losses pro rata, so Morrow builds it above the market. The premium senior pays junior is priced per series along a kinked curve that moves with the size of the junior cushion. The waterfall, the pricing and every rounding direction are checked against an independent integer reference model, proven symbolically with Halmos within stated bounds, and stress tested on a Base mainnet fork through replayed crashes, depegs, defaults and bad debt.

[Repository](https://github.com/saintsama98/Morrow-Finance-Gob) &nbsp;|&nbsp; [Announcement](https://x.com/0xPutAmaterasu/status/2107828803259244663) &nbsp;|&nbsp; [The arithmetic behind tranching](https://x.com/0xPutAmaterasu/status/2102057353072038146)

<br>

## Current Research

Tranching protects a senior holder from losses, but not from waiting to get out. I am researching an exit layer for fixed term credit and tokenized bonds, modelled on the tender option bond that municipal markets have used for decades. A trust holds the slow moving asset and splits it into a senior token with a put at par and a residual token that takes first loss, so exits are refinanced into new owners backed by committed liquidity instead of waiting in an issuer queue. Morrow is the first candidate. The repository is not public yet.

[Read the research thread](https://x.com/0xPutAmaterasu/status/2113636547778203906)

<br>

## Writing

| Piece | About |
| :-- | :-- |
| [Dated Credit and Structured Liabilities](https://x.com/0xPutAmaterasu/status/2096946688997163384) | Why onchain credit still has no liability side |
| [Seven Architectures for Risk Tranching](https://x.com/0xPutAmaterasu/status/2092121207164551274) | Live tranching designs and how they behaved under stress |
| [The Arithmetic Behind Tranching](https://x.com/0xPutAmaterasu/status/2102057353072038146) | The capital model under Morrow, in exact integers |
| [Credit Vaults: Parts Unknown, ACRED](https://x.com/0xPutAmaterasu/status/2108237710255427805) | A tokenized credit fund, from a Morpho loan to its quarterly exit |
| [Where the Fee Hides in the Ten Largest Vaults](https://x.com/0xPutAmaterasu/status/2108942851317064163) | Fee and exit rules across 12.6 billion dollars of vaults |
| [The Limits of Vaultification](https://paragraph.com/@the-finance-sinner/the-limits-of-vaultification-or-dont-overcook-vaults-in-every-defi-recipe) | Why most onchain vaults are constrained escrows |
| [Banana Markets](https://paragraph.com/@the-finance-sinner/banana-markets) | A meta vault routing USDC across four lending venues |
| [Recurring Flywheel Around Stablecoins](https://paragraph.com/@the-finance-sinner/recurring-flywheel-around-stablecoins-unexplored-discussion-about-entrenchment) | Where stablecoin dominance is actually won |

<br>

## Stack

| Area | Tools |
| :-- | :-- |
| **Languages** | Solidity, Go, Python |
| **Testing** | Foundry (unit, fuzz, invariant, fork), Echidna, Medusa, mutation and differential testing |
| **Analysis and verification** | Slither, Aderyn, Halmos symbolic execution (Z3, CVC5, Bitwuzla, Yices), exact arithmetic reference models |
| **Standards** | ERC-4626, ERC-7540, ERC-7887, EIP-2535, ERC-7201, UUPS |
| **Lending and yield** | Morpho (Blue, Midnight, Vaults), Pendle, Aave, Compound, Ethena, Sky, Spark |
| **Credit and structured products** | Centrifuge, Maple, Pareto, Securitize, Strata, Royco |
| **Infrastructure** | Chainlink, Zama |

<br>

## Contact

Open to engineering and research roles in onchain credit, vaults and structured products.

[X: @0xPutAmaterasu](https://x.com/0xPutAmaterasu) &nbsp;|&nbsp; [adiii.eth.limo](https://adiii.eth.limo) &nbsp;|&nbsp; [adiiiresearch@gmail.com](mailto:adiiiresearch@gmail.com)
