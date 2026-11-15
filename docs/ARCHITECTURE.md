# I_Mortal public architecture overview

This is a product-level explanation of the intended boundaries. It omits operative policies, deployment topology, trust anchors, service identities and implementation details.

## Client experience

Clients present account information, proposals, approvals and outcomes. They must identify the account, device, network and action accurately. The target scope includes Windows, Linux, Android, iOS, macOS and browser experiences, with equivalent security requirements.

## Untrusted proposals and external information

Assistant output, venue responses, website content and user-entered instructions are treated as untrusted data. The assistant should receive only scoped, sanitized information needed for the requested function. It must not gain operator tools, arbitrary filesystem access, credentials, operative policy or signing material.

Prompt filtering is one layer. Effective protection also requires OS isolation, typed interfaces, narrow privileges and independently enforced authorization. These deployment and device properties are not established by a successful conversation test.

## Protected action services

Consequential actions need independent checks at the boundary where the effect occurs. The intended checks cover exact intent, current identity, account and network scope, consent, limits and revocation. Policy selection and updates must remain outside model control.

Rejected or uncertain requests must not be converted into successful actions by a fallback path. Public interface navigation should remain usable when a protected feature is unavailable, with an accurate explanation of its status.

## Custody and signing

The owner authentication key is intended to remain device-bound. Execution signing requires separately authorized, non-exportable signing capabilities. Short-lived task authorization, hardware protection and independent approval are design requirements whose complete production implementation is still pending.

Public keys, fingerprints and public receipts can identify or verify an operation. Cryptographic signing itself requires private material to be used internally within an accepted protected boundary. Applications and models must not receive that material.

## Durable records and independent evidence

Requests need durable reservations, replay controls and exact outcome records. Database commits, broadcast acknowledgments and confirmations have different meanings; an uncertain acknowledgment must not be shown as completed success.

Independent checkpoints are intended to detect inconsistent or rolled-back state. A database cannot establish independence by returning its own stored hash. Current work includes consistency codecs and disposable tests; real independent services, authenticated channels and recovery procedures remain prerequisites.

## Release acceptance

Source checks, software tests, transformed-package inspection, hardware tests and production service acceptance are separate milestones. Obfuscation does not protect an embedded secret or replace isolation. A release needs the complete set of applicable evidence, including each target platform's device and runtime behavior.

The current project keeps production authorization blocked while these prerequisites remain incomplete.
