# Security

## Reporting a vulnerability

Report it privately, through [GitHub's private vulnerability reporting](https://github.com/InsaneArts/jolt-app/security/advisories/new). Never in a public issue or discussion.

Please include what an attacker gains, the steps to reproduce it, the version of Jolt and of macOS, and anything that narrows down where it lives. A proof of concept helps.

You will get a first reply within a few days. If the report holds, you will be told when a fix ships, and credited in the release notes unless you would rather not be.

## Supported versions

Only the latest release. Jolt updates itself and checks for updates once a day, so the latest release is where a fix lands.

## What is in scope

Jolt itself and the backend it talks to: the launcher, the companion, the update mechanism, licensing, and the API at the address a release build is built against.

Some things that would be interesting:

- Making Jolt run something it should never offer, such as a command the [capability policy](https://usejolt.app) excludes.
- Getting query text, menu titles, filenames, or file contents off a Mac in a way the privacy rules say should not happen.
- Getting an update installed that was not signed with Jolt's EdDSA key, or otherwise subverting Sparkle.
- Forging, extending, or transferring a license or trial; reading another installation's credentials out of the Keychain.
- Anything a scripting dictionary of a third-party app can make Jolt do that Jolt does not intend.

## What is not in scope

- Reports produced only by a scanner, with no working attack behind them.
- Missing hardening that leads nowhere on its own.
- Attacks that need an already-compromised Mac, physical access with the screen unlocked, or admin rights you already have.
- Denial of service by volume against the backend.
- Bugs in macOS itself, or in Apple's APIs, that Jolt only passes through.

Do not test against other people's Macs, other people's licenses, or the production backend at a rate that affects anyone else. Test against your own installation.
