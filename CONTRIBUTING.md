# Contributing

Jolt's source code is not in this repository, so there is nothing here to send a pull request against. What this repository takes is reports, and they are worth more than they sound: most of what Jolt gets wrong is one query away from being obvious, and only the person who typed it knows what they meant.

## The three kinds of report

**A bug.** Something does not work. [Open one](https://github.com/InsaneArts/jolt/issues/new/choose) with the steps, the version, and what you expected. Logs help most of all:

```sh
log stream --predicate 'subsystem == "dev.gomareli.jolt"'
```

Jolt writes no queries to its log. Read what you paste anyway, before you paste it.

**A wrong result.** Jolt understood you and picked the wrong command, or found nothing. This has its own form, because the useful part is the pair: what you typed, and the row you wanted. A wrong answer is usually fixed by telling Jolt what a command is for, which is a small change, so these get handled quickly.

**A request.** Something Jolt should do and cannot. Say what you are trying to get done first, and the feature second — the task is the part that cannot be guessed. If it is still half-formed, [Discussions](https://github.com/InsaneArts/jolt/discussions) is the better room.

## Before you open one

Search first; the same query often comes up twice. Be on the latest release, or say which one you are on and why. One report per thing — two bugs in one issue means one of them gets forgotten.

## What not to post

No license keys, no API keys, no credentials. No filenames, screenshots, or logs that carry someone else's data, or yours. A made-up example that shows the same problem is always fine.

Security issues do not go in public at all: [SECURITY.md](SECURITY.md) says where they go.

## The code of conduct

[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md), and it is short. Be plain, be kind, stay on the topic.
