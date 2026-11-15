# I_Mortal

### A wallet and controlled trading-agent platform in development

I_Mortal is being built to bring wallet management, user-approved transactions and bounded automated trading into one application. The intended experience combines a familiar wallet interface with an assistant that can explain information and prepare actions, while protected services independently control consequential operations.

**Status: pre-production development. This repository contains public project documentation only. There is no production wallet or live-trading release available from this repository.**

Development includes client interfaces, account and device flows, exchange integration work, transaction records, and security-boundary components. A substantial part of the current work tests what must be rejected: malformed requests, substituted identities, unauthorized actions, repeated requests and uncertain outcomes.

## What the platform is intended to provide

| Area | Intended experience | Current public status |
| --- | --- | --- |
| Wallet | View assets and networks, review balances and transaction activity | Preview/interface and backend development; production acceptance pending |
| User transactions | Prepare swaps, sales, purchases, sends and receiving addresses | Protected transaction lifecycle is not accepted for public live use |
| Assistant | Read scoped information, explain results and prepare proposals | Current software boundary tests pass with public doubles; live service acceptance pending |
| Trading agent | Trade within an explicitly approved venue, pair, budget and duration | Control-boundary development; no qualified production trading release |
| Accounts and custody | Device linking, recovery and optional shared custody | End-to-end production and hardware acceptance pending |
| Clients | Windows, Linux, Android, iOS, macOS and browser experiences | Shared requirements apply across clients; complete platform parity is not yet verified |

Receiving, purchasing and exchange support each require their own network-specific implementation. A visible network or venue in a preview is a browsing capability, not confirmation that live transactions are enabled.

## What has been accomplished

Recent work has produced repeatable, scoped software evidence:

- Public signed-response verification and request-lifecycle tests passed, including wrong-key, nonce-mismatch, signature-corruption and replay-denial cases.
- Disposable database tests exercised reservation uniqueness, consume-once behavior, actual competing transactions and persistence after a graceful restart.
- A native database-driver diagnostic tested real parameter binding and deliberately lost commit/close acknowledgments without reporting success.
- Pending checkpoint events were tested for atomicity, permission separation, partition isolation and agreement with a separate transition codec.
- Current conversation, proposal and bridge checks rejected execution-shaped tool calls, caller substitution and inappropriate authority forwarding.
- Build-policy regressions verified rejection of removed restrictions, model policy-access claims and forged acceptance flags.

These results are internal development diagnostics, not an independent security audit, production attestation or a capacity guarantee. Test doubles are identified explicitly in the [verified progress](docs/VERIFIED_PROGRESS.md) record.

## Security direction

The design requires device-bound owner authentication, protected non-exportable signing, narrowly scoped authorization, and enforcement outside the assistant or trading model. Model output and external content are untrusted data. Application functions must pass typed validation and current authorization at the protected action boundary.

Public keys and fingerprints identify or verify signing authority; private signing operations still require protected cryptographic hardware internally. Public identifiers are not a replacement for private-key cryptography.

Some of these requirements have software implementations and diagnostics. Complete deployed OS isolation, independent security services, hardware-backed custody, and acceptance across every target platform remain unfinished. Production builds and signing remain blocked pending acceptance.

## Explore the project

- [Product and intended user journeys](docs/PRODUCT.md)
- [Public architecture overview](docs/ARCHITECTURE.md)
- [Verified software milestones and their limits](docs/VERIFIED_PROGRESS.md)
- [Work remaining before production](docs/ROADMAP.md)
- [Security reporting](SECURITY.md)
- [Publication scope](NOTICE.md)

**Snapshot: November 14, 2026.** This documentation describes development status, not a commitment to a release date, investment return, token launch or availability in a particular country.
