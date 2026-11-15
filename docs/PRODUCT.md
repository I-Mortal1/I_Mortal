# I_Mortal product overview

## Purpose

I_Mortal aims to give users a coherent place to manage wallet activity and explicitly bounded trading automation. The interface should make it clear which account, network, asset and venue an action uses, what the user is authorizing, and what actually happened afterward.

The project is in development. The following journeys describe the intended product and acceptance requirements, not a list of publicly activated services.

## Wallet experience

Client work includes wallet views, asset and network discovery, asset details, transaction screens, account settings and exchange-connection interfaces. Network browsing should filter assets by the selected network and preserve an all-assets view. Wallet search should operate on the user's own holdings where that context is selected.

Asset discovery, quoted prices, owned balances and executable trading support are different kinds of information. Each needs an appropriate source and freshness label. A missing balance or quote must be shown as unavailable rather than replaced with fabricated data.

Preview client work exists alongside the protected backend components. Final visual, accessibility, device, packaging and feature-parity acceptance is still required on all supported platforms.

## User-approved transactions

The intended manual workflow covers swaps, sales, purchases and sends. The user should see the exact asset, network, recipient or route, amount and costs before approving an action. An assistant may help prepare a proposal, but approval and execution must remain with the independently authorized transaction path.

Each consequential manual action requires its own approval. The device must participate in the accepted authentication flow, and the transaction must pass the appropriate simulation, authorization, signing, broadcast and confirmation checks.

Receiving requires a verified address for the selected network and deposit tracking. Purchase availability also depends on the relevant venue or on-ramp. Neither is established merely by displaying a button.

Transaction records are intended to cover user and agent activity, copyable transaction identifiers, action details, status, gas and applicable fees. Production acceptance must still prove reconciliation, incoming-deposit indexing and correct handling of delayed confirmations or chain reorganizations.

## Assistant and automated trading

The assistant is intended to explain verified information and prepare structured proposals. Public development tests currently cover conversation timing, caller continuity, malformed tool responses and rejection of execution-shaped requests.

The agent workflow requires an explicit venue, network, trading pair, live or paper mode, duration and budget/limits. Initial authorization should establish a bounded trading session; subsequent actions must stay within that independently enforced authorization. Extending a session or increasing its limits requires a new approval.

The intended bot controls let users start an authorized session, request its status, and stop or revoke it. A stop request must distinguish revoked authorization from a confirmed worker shutdown. It cannot reverse an already submitted transaction or filled order.

Manual actions and autonomous agent trades use separate authorization and signer paths. Connecting an account must not itself authorize trading. Paper activity, live activity and account-wide balances must remain clearly distinguishable.

The trading model is not qualified for production, and no profitability or investment-performance claim is made. Model qualification remains deferred until the wallet and security foundations are accepted.

## Exchange integration status

DEX integration work includes Uniswap, PancakeSwap, Aerodrome, Raydium and Jupiter. Each venue/network combination still requires accepted market discovery, token validation, routing, simulation, execution and reconciliation. This repository does not claim these venues are live or uniformly supported.

Hyperliquid requires its own account, authorization and fee treatment. Centralized-exchange integration is deferred; its account, custody, access and program requirements must be resolved separately. Users should not assume funds held in one account can be traded on every venue without venue-specific funding requirements.

Network gas, exchange charges and platform charges must be clearly disclosed and reconciled. This overview does not announce launch pricing, free transactions or completed fee collection.

## Accounts, devices and shared custody

Production work remains for durable registration, verification messages, sign-in, session refresh, logout/revocation, deletion, device linking and recovery. Device possession and biometric behavior must be accepted on real hardware.

Shared custody additionally needs participant consent, approval thresholds, withdrawal rules, revocation and lost-device recovery. A packaged recovery module is not evidence that the complete custody journey works.
