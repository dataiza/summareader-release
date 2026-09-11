# SummaReader — downloads

A reader that pulls in what you follow — feeds, articles, YouTube, Mastodon,
Nostr — summarizes it, and keeps the result in step across your own devices.

**This repository holds released builds and nothing else.** No source, no issue
tracker, no development. It exists so that downloads have a stable address:
every release below is a plain file you can fetch without an account.

Get the latest at **[Releases](../../releases/latest)**.

---

## What it does

Things arrive — RSS and Atom feeds, web pages, YouTube channels, Mastodon,
Nostr — and the app extracts the readable article from each, keeps it, and can
summarize it.

**Your library never leaves your devices in readable form.**

**Summarization runs on-device by default**, using a model you download once.
You can point it at your own server or a cloud API instead — that is the only
time article content goes anywhere, and only if you choose it.

**Sync is optional, end-to-end encrypted, and self-hosted.** There is no hosted
service. The only sync server is one you run yourself; it holds ciphertext and
cannot read any of it.

No accounts. No analytics. No telemetry. No crash reporting.

## Free and premium

The builds here are the **free** product, and it is a complete reader: getting
things in, reading them, saving them, summarizing an article when you ask, and
syncing across your own devices — with no limit on how many sources you follow.

**Premium** adds what makes a large library navigable — search, filters, tags,
multiple lists, highlights — and summarizing that happens without being asked.
It is a separate application, sold separately, and is not distributed here.

## Installing

Builds are **64-bit only**. Android is arm64; desktop is x86-64.

### Android

Download the `.apk`, then allow your browser or file manager to install unknown
apps when the phone asks. The `.aab` files some projects publish are not here on
purpose — an App Bundle is what a store uploads, not something a phone can
open.

### Linux

There is no installer yet. A build is a directory you run out of:

```sh
tar xzf summareader-free-linux-x64.tar.gz
./bundle/summareader
```

You need GTK 3 and libsecret present. On Debian or Ubuntu that is
`libgtk-3-0` and `libsecret-1-0`; on Arch, `gtk3` and `libsecret`. libsecret is
where the app keeps its sync token and encryption keys — without it, it falls
back to a file and says so.

### macOS

Unzip and move `SummaReader.app` to Applications. These builds are **not yet
signed or notarised**, so the first launch has to be right-click → *Open*
rather than a double-click; macOS refuses the double-click and does not explain
itself.

### Windows

Not yet available. The build target exists but has never produced a working
binary, and there is no on-device summarization engine for Windows.

## First run

If you want summaries computed on your own machine, the app offers to download
a model once. It is about **2.6 GB** and lands in the app's own data
directory. Everything else works without it, and you can instead point the app
at your own endpoint or a cloud API in Settings.

## Updates

These builds do not update themselves yet. Watch this repository's releases, or
check back here.

## Licence and privacy

SummaReader is proprietary software. Copyright © 2026 Dataiza s. r. o.,
Slovakia. Downloading a build grants you the right to use it; it does not grant
the right to redistribute it or to take it apart.

The open-source components the app is built from keep their own licences, which
are reproduced inside the app under **Settings → About → Open-source licences**.

The privacy policy is at
<https://summareader.dataiza.sk/privacy.html>.
