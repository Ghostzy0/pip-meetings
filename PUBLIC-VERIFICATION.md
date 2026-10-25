# Verification and limits

23 October 2026. **Experimental native macOS source.** File-fed local transcription and selected persistence/recovery paths have measured evidence. Native microphone/system recording and complete reference fidelity remain unaccepted.

## Clean-export build inputs and local package checks

The current clean Custom source build-input manifest is SHA-256 `aae4638139564a77ac26934cd04ee83e38fb53f0d2e848ccd06493fc1b23b1a4`; the shared engine input is `c3c68bb96387f3ea1a2d13aa6b3213360273e0d46a96ccc9523c819dfafe4cfb`. Historical local checks used the preceding Custom input digest `37c860ff4cfa6e393d018ccc91c70328be408d54101e6c66b5081c01777f5807`: the default Pip edition ran `scripts/test-native.sh` with 118 selected tests and 0 failures, and `scripts/build-native.sh` built Pip with source receipt, bundle identity, and strict ad-hoc signature verification passing. The current source includes the same compiler-only transcript-view helper extraction as Replica; this exact source digest has not yet been built locally. The local package is not notarised or included in this repository. The shared release-integrity suite passed 14/14 focused Python tests. These checks do not extend to a local package claim for Neutral Plus or Pip Plus; hosted per-edition results are listed below.

## Hosted clean-export CI

The public workflow uses read-only checkout permissions, macOS 26, selected native regression tests, per-edition packaging, and AudioTap tests. [Initial Custom main run](https://github.com/Ghostzy0/pip-meetings/actions/runs/40120729559) tests the preceding app-input digest `37c860ff4cfa6e393d018ccc91c70328be408d54101e6c66b5081c01777f5807`. At the latest check, `baseline-enhanced` and `pip` completed successfully through speech setup, native regressions, packaging, and AudioTap verification; `pip-enhanced` was still running its native regressions. This is not a completed matrix. The current transcript-view helper extraction has digest `aae4638139564a77ac26934cd04ee83e38fb53f0d2e848ccd06493fc1b23b1a4` and awaits its pull-request CI run.

Verified host: Apple Silicon arm64, macOS27.0.1, Xcode27.1/Swift6.4. Intended source target is macOS14.2+ with Swift tools6.2+. Intel and other hosts remain unverified. Local packages are **ad-hoc signed, not Developer ID signed or notarised**. A local build does not establish native recording acceptance.

## Network-denied file transcription

The app owner ran each exact executable below with macOS process policy `(deny network*)`, pinned WhisperKit1.1.0 tiny.en resources and a separate synthetic data directory. All four exited0, producing7 ordered timestamped segments and the complete expected normalized text from the13.98-second synthetic two-voice script. Timestamps stayed chronological and within the source audio. No speaker labels were emitted.

| Local package | Exact tested executable SHA256 |
| --- | --- |
| Neutral Core Replica | `736296eefbaf4d3d275308dfdc6b34846f7b6b96311cc8be997ffdd906e32c9f` |
| Neutral Plus | `195ca8960e40560005e28f9499531c72ac8a4e4166989cfc24c29047fbc30efd` |
| Pip Core | `f405f617bb69675fbdc3c9826cccff08436128aea43209f987d27478bced5566` |
| Pip Plus | `0abb46e3d178b0757c9b556ac497460dc90deca250366e4d83440b6ce048826f` |

Fixture SHA256: `a1e4d2ab03c971b10b8b82839eafce0bfa35f0b280266b85e6ed3533507b7a71`. These are local artifact results, not hashes for an asserted downloadable app. Elapsed time ranged roughly1.1–4.7seconds on this shared host; cache state was not controlled. This single scripted fixture is not a broad accuracy, speaker attribution or performance benchmark. Later exported/rebuilt packages need their own receipts.

Pinned speech setup verified28 files totaling80,389,997bytes. Model/tokenizer revisions, hashes and licences are in [local speech setup](docs/LOCAL-SPEECH.md). Setup downloads are explicit; the recorded transcription tests used no network. No model weights are included in source Git.

## Foundation and reference boundaries

The unchanged MIT Meeting Transcriber0.8.1 foundation at `a4f6af6df2674bc4e18097084a128af469823fab` built separately and passed an earlier synthetic LocalVQE echo probe with57dB reduction. That is echo-processing evidence, not native recording or ASR acceptance. Product builds constrain providers, automatic watcher, updater and debug transports; they share one local functional core.

The neutral replica's home → note → bottom transcript drawer follows an observed Granola7.668.2 vendor demo. It uses original/licensed code and system typefaces. Calendar connection, hosted sharing, cloud assistant/enhancement and reliable speaker identity are unavailable; no complete Granola equivalence is claimed. The custom Plus styles add the same local Open actions projection, with filtering/order/reopen regressions.

## Remaining acceptance

- Clean exported repository setup/builds and final downloaded source/artifact recovery.
- Current native note/transcript/decision/action editing, source links, search/export/reopen, archive recovery and Plus interaction.
- Explicit native microphone/system recording, pause/resume/stop and interrupted capture with actual user grants. No such grant or live capture pass is established here.
- Current screenshots, bounded windows, keyboard/focus, light/dark, reduced motion, VoiceOver, long recordings and measured idle resources.

Source, tests, a successful file transcription and a screenshot are distinct evidence. Review transcripts and exports before use; manual notes/actions do not imply AI extraction. Store files and recordings are not encrypted by this app. No production, stable, signed/notarised or complete offline-device acceptance claim follows from these checks.

## Exported fixture scope

This source export excludes Git-ignored local `.wav` and `.aiff` files, including audio fixtures. The selected `scripts/test-native.sh` regression lane does not use those fixture files. Fixture-dependent and opt-in model-quality tests are not thereby accepted. Some guarded tests skip when audio is absent, while structural `QualityFixtureTests` require the excluded WAVs and fail without them. The full upstream test suite has not been claimed as passing from this clean export.


## Manual walkthrough status (24 October 2026)

The parent tested the frozen Neutral Core Replica executable (SHA-256 `736296eefbaf4d3d275308dfdc6b34846f7b6b96311cc8be997ffdd906e32c9f`). In the first run, a synthetic note persisted but repeated accessibility/coordinate attempts did not open its detail. CUA binding timed out twice while the copied synthetic fixture was under Documents. A process sample showed the main thread blocked in `chmod` called during `PipMeetingLibrary.init` line 160. This observed stack does not identify whether the filesystem, operating system, or another launch condition caused the stall. The parent then reran the same binary with the copied synthetic record under a separate temporary-root data directory: the row opened, edited title and notes saved, Back/list/reopen retained both, and a manual action saved with the accessibility label `Your own note`. This is a partial pass for note detail, edit/save/reopen, and manual action creation in that one session; no source patch was made, and the storage-path cause remains unconfirmed. It does not establish full note CRUD or export, action completion/removal, immutable-source behavior, recording, ASR, permissions, accessibility coverage, or complete reference fidelity. The custom editions' packaged walkthrough remains pending; no result is inferred from this Replica run. Native microphone/system recording and permission acceptance remain unverified.

## Package preservation candidate

This candidate adds source-level package-promotion safeguards and focused filesystem regressions. Its app build-input manifest SHA-256 is `c268f5e6b3356be8c7509b5027198fbcef72c1c59a31a92efbc92f307012efc3`. The local focused Python suites passed on the candidate scripts (12 promotion tests and 14 release-integrity tests); wrapper integration used stubbed Swift, codesign, plist, and resource tools. Those checks are not a native build, signed-package acceptance, or runtime/device validation. Hosted candidate CI is pending; existing native/package evidence above applies to its recorded earlier source identity.
