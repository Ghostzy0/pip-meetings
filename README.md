# Pip Meetings

A native macOS workspace for local meeting transcripts, decisions and actions. Built on the MIT Meeting Transcriber audio and recovery foundation, with an original Pip interface.

**Experimental custom product, in development.** This export contains Neutral Plus, Pip Core and Pip Plus; Pip Core is the default. Granola is a workflow reference. No affiliation or complete equivalence is claimed. Recording acceptance needs the user's native permissions. See [public verification](PUBLIC-VERIFICATION.md) for exact builds and checks.

**Known native limits (25 Oct 2026):** The source now validates a newly created library root before canonicalizing its path; focused internal library/persistence and root-link tests passed, but were not rerun on this public candidate. A private diagnostic Pip build saved a synthetic first meeting, opened its detail, and saved a title and notes; the first-create process ID was not sampled. In a separate run, an existing synthetic note reopened after its live process identity was verified against the intended frozen app. These checks do not establish recording, complete UX, or reference parity.

[![Verify exported Meetings product](https://github.com/Ghostzy0/pip-meetings/actions/workflows/verify.yml/badge.svg?branch=main)](https://github.com/Ghostzy0/pip-meetings/actions/workflows/verify.yml) · [Verification](PUBLIC-VERIFICATION.md) · [Report an issue](https://github.com/Ghostzy0/pip-meetings/issues/1) · [Neutral Core Replica](https://github.com/Ghostzy0/pip-meetings-replica)

## What it does

- Explicit native recording and local audio processing through the Meeting Transcriber foundation.
- A local library for transcripts, editable notes, decisions/actions and source references.
- Local speech files and text exports. No account or hosted runtime is required for Pip.
- A separately buildable baseline for comparison, with original upstream notices.

The Neutral Plus and Pip editions remove external note-provider, automatic watcher, updater and debug-control routes at the code boundary. The upstream provenance build is not part of these public products. See native/THIRD-PARTY-NOTICES.md and docs/LOCAL-SPEECH.md for dependencies and downloaded weights.

## Build the custom product

macOS 14.2+ on Apple Silicon is the intended recording platform. The verified build host uses Xcode 27.1/Swift 6.4; Swift tools 6.2+ (Xcode 26+) is required. Intel/older OS native acceptance is unverified. The default edition is `pip` (Pip Meetings). Available variants: Neutral Plus (`baseline-enhanced`), Pip Core (`pip`), Pip Plus (`pip-enhanced`).

```sh
scripts/test-native.sh
scripts/build-native.sh
open 'dist/pip/Pip Meetings.app'
```

Build another enabled variant explicitly:

```sh
scripts/build-native.sh baseline-enhanced
scripts/build-native.sh pip-enhanced
```

Build scripts download pinned Swift dependencies/binary artifacts and a small hash-verified Apache 2.0 LocalVQE echo file. No paid service is needed. They create ad-hoc signed applications in `dist/`; these are not Developer ID signed or notarised. Never disable macOS security globally. Use a locally built app or inspect the published prerelease's actual signing/known-issue notes. See [edition map](docs/EDITIONS.md).

For speech, run `python3 scripts/setup-speech.py`, then choose its output folder in Pip. This explicitly downloads about 80.4 MB of hash-verified tiny.en files. Keep both the CoreML and tokenizer directories. Speech recognition is fallible; read the transcript before using it. [Speech setup and licences](docs/LOCAL-SPEECH.md) · [Short AI setup prompt](docs/AI-SETUP.md).

## Privacy and permissions

Only record with the participants' consent. Microphone and system-audio access are native OS approvals made by the user. Do not use real meetings for development. A headset helps reduce acoustic echo; source labels and automatic diarisation must not be assumed to identify people accurately.

Pip's meetings, recordings and notes live in its own Application Support directory. Speech files stay in their chosen local folder. Local storage is not encrypted by this app; OS storage protection remains relevant. Exported files are separate copies and must be reviewed before sharing. The application must not upload meeting content. Model/setup downloads are distinct from processing content offline; see the actual network-denied test evidence in [verification](PUBLIC-VERIFICATION.md).

No upstream provenance build is included in this export. The distributed editions do not import another app's credentials. Model downloads and native grants do not establish complete offline or microphone acceptance.

## Help, changes and contributing

Maintainer: [Ghostzy0](https://github.com/Ghostzy0). [Change notes](CHANGELOG.md), [security](SECURITY.md), [contributing](CONTRIBUTING.md), [upstream provenance](UPSTREAM.md), [Granola workflow documentation](https://docs.granola.ai/help-center/taking-notes/transcription). Use repository issues for reproducible bugs without private audio, screenshots or account data. Do not post sensitive information in public reports.

Pictures and release links are added only when genuine synthetic renders and reviewed artifacts are available. There is no hosted runtime dependency.

[Frequently asked questions](docs/FAQ.md) · [Move existing material](docs/MIGRATION.md)
