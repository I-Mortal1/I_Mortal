# I_Mortal production roadmap

These are acceptance priorities, not release dates. A completed software component is only one input to a production decision.

## 1. Security boundaries and release integrity

Reconcile exact-source evidence, finish build-entrypoint coverage, and accept actual OS/process/IPC/network isolation. Keep models and application harnesses separate from operative policy, credentials, arbitrary files, operator tools and signing material. Validate protected signing context, package hardening, dependency provenance and each platform's runtime behavior.

## 2. Independent services and protected runtime

Complete independently controlled trust, revocation, release approval, durable checkpoints and protected runtime admission. Resolve bootstrap time, authenticated service enrollment, pending-state reconciliation, recovery and outage behavior. Software fixtures cannot stand in for these services.

## 3. Accounts and custody journeys

Complete durable registration, verification messages, login, refresh, logout/revocation and deletion. Accept device linking/unlinking, real biometric possession, recovery and shared-custody consent/threshold/withdrawal/revocation behavior. Verify delivery and reconciliation of account, device and custody notifications.

## 4. Wallet and exchange execution

Accept wallets separately on each supported chain. Complete venue-specific discovery, token validation, routing, simulation and protected execution. Verify exact approval, signing, broadcast, confirmation, incoming deposits, reorganizations and gas/fee settlement. Keep unsupported venue/network combinations unavailable without inventing data or silently widening authorization.

## 5. Reliability, capacity and operations

Complete durable queues, bounded partitions, backpressure and safe writer fencing. Accept database isolation, backups, restore/failover and reconciliation. Deploy observability and incident response, then run realistic load and outage tests. No user-capacity number is claimed before measurement.

## 6. Platform and distribution acceptance

Complete feature and security parity on Windows, Linux, Android, iOS, macOS and browser bridges. Validate real devices, accessibility, signing bridges, final package contents and distribution requirements. Preview testing and successful diagnostic compilation do not imply production-store acceptance.

## 7. Trading-model qualification

Keep model qualification last, after the preceding foundations are accepted. Evaluate strategy artifacts, paper/live separation, risk limits, reproducibility and operational behavior. No automated trading or profitability claim should be based on an unqualified model.

## Participation

This repository provides a public overview. It does not contain the private implementation or accept deposits, credentials, recovery phrases or wallet keys. Public feedback about the documentation or intended user experience can be directed to the maintainer's GitHub profile. Use the private route in [the security notice](../SECURITY.md) for potentially sensitive findings.
