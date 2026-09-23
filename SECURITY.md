# Security

## Reporting a vulnerability

Report it privately, through [GitHub's private vulnerability reporting](https://github.com/InsaneArts/jolt/security/advisories/new). Never in a public issue or discussion.

Please include what an attacker gains, the steps to reproduce it, the version of Jolt and of macOS, and anything that narrows down where it lives. A proof of concept helps.

Reports are read by the maintainers of Jolt. If one holds, you will be told when a fix ships, and credited in the release notes unless you would rather not be.

## Supported versions

Only the latest release. Jolt updates itself and checks for updates once a day, so the latest release is where a fix lands.

## What is in scope

The released Jolt app: the launcher, what it reads through the Accessibility API, what it sends to the Jolt backend, and the update mechanism.

Some things that would be interesting:

- Making Jolt run something it should never offer, or run a command with a value it should have refused.
- Getting query text or menu titles off a Mac in a way "What leaves your Mac" in the README says should not happen.
- Getting an update installed that was not signed with Jolt's EdDSA key, or otherwise subverting Sparkle.
- Reading credentials, such as the license key or the session in its Keychain, out of a place only Jolt should reach.
- Anything another app on the Mac can make Jolt do that Jolt does not intend.

## What is not in scope

- Reports produced only by a scanner, with no working attack behind them.
- Missing hardening that leads nowhere on its own.
- Attacks that need an already-compromised Mac, physical access with the screen unlocked, or admin rights you already have.
- Denial of service by volume against the Jolt backend or the TypeSafe API.
- Bugs in macOS itself, or in Apple's APIs, that Jolt only passes through.

Do not test against other people's Macs, and do not hammer the Jolt backend. Test against your own installation.
